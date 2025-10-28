# 🚀 **Lab: Implement GitHub Actions for CI/CD**

**Based on:** Microsoft Learning Lab — *Implement GitHub Actions for CI/CD*  
**Goal:**  Set up a GitHub Actions workflow to build, test, and deploy the **eShopOnWeb** app to Azure App Service.

---

## 🧰 **Prerequisites**

| Requirement | Description |
|--------------|--------------|
| 💻 GitHub Account | Create or use an existing GitHub account |
| ☁️ Azure Subscription | With **Contributor/Owner** access |
| 🌐 Web Browser | Chrome / Edge recommended |
| ⚙️ Azure CLI | Optional (for local setup) |

---

## 🧩 **Lab Outline**

1. 🔹 Import `eShopOnWeb` repository into GitHub  
2. 🔹 Create Azure Service Principal & Resource Group  
3. 🔹 Configure GitHub Secret (`AZURE_CREDENTIALS`)  
4. 🔹 Edit and run GitHub Actions workflow  
5. 🔹 Verify deployment in Azure  
6. 🔹 Clean up Azure resources  

---

## 🧪 **Exercise 1 — Import Repository**

1. Sign in to **GitHub** → click **New → Import a repository**  
2. Enter the source URL:  
   ```
   https://github.com/DevOpsifyZen/eShopOnWeb123.git
   ```
3. Name your repo (e.g., eShopOnWeb) → **Begin Import**
4. After import, open the repo → Go to **Settings → Actions → General**
  * ✅ Allow all actions and reusable workflows
  * 💾 Save changes

💡 **Check:** Your repo now contains the eShopOnWeb files and Actions are enabled.

---

## Exercise 2 — Setup Azure access & GitHub secret

### Task 2.1 — Create Resource Group
1. Open Azure Portal.  
2. Navigate to **Resource groups → + Create**.  
   - Name: `rg-eshoponweb-<YOUR_ALIAS>`.  
3. Click **Create**.

### Task 2.2 — Create Azure Service Principal
1. Open **Cloud Shell** (Bash mode).  
2. Run:

```bash
az ad sp create-for-rbac \
  --name GH-Action-eshoponweb \
  --role contributor \
  --scopes /subscriptions/SUBSCRIPTION-ID/resourceGroups/RESOURCE-GROUP \
  --sdk-auth
```
4. Copy the JSON output (contains clientId, secret, tenant, etc.)
5. (If needed) Register the Web provider:
```
az provider register --namespace Microsoft.Web
```

### 🔒 Step 2.3 — Add GitHub Secret

1. In **GitHub Repo → Settings → Secrets and variables → Actions → New repository secret**
  * **Name:** AZURE_CREDENTIALS
  * **Value:** paste the JSON from Azure CLI output
2. Click **Add secret**

✅ Check: Secret `AZURE_CREDENTIALS` is present in the repository.

---

## ⚙️ Exercise 3 — Configure the GitHub Actions Workflow

1. In your repo, open: `.github/workflows/eshoponweb-cicd.yml`
2. Uncomment the `on:` trigger (for pushes to `main`, `workflow_dispatch`).
3. Update `env:` section with your values:
  * `RESOURCE-GROUP:` rg-eshoponweb-<YOUR_ALIAS>
  * `LOCATION:` e.g., eastus
  * `UBSCRIPTION-ID:` your Azure subscription ID
  * `WEBAPP-NAME:` unique name (e.g., `eshoponweb-<youralias>`)
4. Commit the change.

***Note:*** Workflow will start automatically after commit.

---

## 🧩 Exercise 4 — Monitor & Verify Deployment

1. Go to the Actions tab in GitHub
2. Watch the workflow jobs:🧱 `buildandtest`🚀 `deploy`
3. Wait until both jobs show ✅ success
4. After success, Go to Azure Portal → Resource Group → App Service
5. Copy the app’s URL → open in your browser

🌐 **Check:** Your web app (eShopOnWeb) is live!


---

## 🧹 Exercise 6 — Cleanup

1. In Azure Portal → Resource Groups → `rg-eshoponweb-<YOUR_ALIAS>`
2. Click **Delete resource group**
3. Optionally delete your GitHub repo

✅ Cleanup complete — lab successfully finished!

---

## 📚 References

[Microsoft Learn — Implement GitHub Actions for CI/CD](https://microsoftlearning.github.io/AZ400-DesigningandImplementingMicrosoftDevOpsSolutions/Instructions/Labs/AZ400_M02_L05_Implement_GitHub_Actions_for_CI_CD.html?utm_source=chatgpt.com)

[GitHub Docs — Actions Workflows](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax)

[Azure Docs — Deploy Web Apps](https://learn.microsoft.com/en-us/azure/app-service/)
