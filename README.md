# Crimson Cipher on Firebase Studio

This is a Next.js application built in Firebase Studio.

## How to Deploy Your Site

You can deploy this application directly to Firebase Hosting for free. Follow these steps to get your site live on the web and connect your custom domain (e.g., IAIWAF.com).

### Step 1: Set Up Your Local Environment

1.  **Navigate to Your Project Directory:** Before running any commands, make sure you are inside your project's root folder in your terminal. This is the folder that contains `package.json` and `firebase.json`.

2.  **Install Firebase CLI:** If you haven't already, install the Firebase Command Line Interface on your local machine. You will likely need administrator privileges to install it globally, so use `sudo`:
    ```bash
    sudo npm install -g firebase-tools
    ```

3.  **Login to Firebase:** Run `firebase login` to authenticate with your Google account. This will open a browser window for you to sign in.
    ```bash
    firebase login
    ```

4.  **Update `.firebaserc`:** Open the `.firebaserc` file in your project and replace `<YOUR_FIREBASE_PROJECT_ID>` with your actual Firebase Project ID. You can find this ID in your project settings in the [Firebase Console](https://console.firebase.google.com/).

### Step 2: Deploy to Firebase Hosting

Once you are logged in and in the correct project directory, run the deploy command:

```bash
firebase deploy
```

This command will build your Next.js app and deploy it to Firebase's global hosting service.

### Step 3: Connect Your Custom Domain

After your app is deployed, you can connect your domain in the Firebase Console.

1.  **Open Firebase Console**: Navigate to your project in the [Firebase Console](https://console.firebase.google.com/).
2.  **Go to Hosting**: In the left-hand menu, find the **Build** section and click on **Hosting**.
3.  **Add Custom Domain**: Click the **"Add custom domain"** button.
4.  **Enter Domain Name**: Type in `IAIWAF.com` and follow the setup wizard.
5.  **Verify Ownership**: Firebase will provide a **TXT record**. You must add this record to the DNS settings at your domain registrar (the service where you bought your domain). This is a required step to prove you own the domain.
6.  **Add A Records**: Once verified, Firebase will give you one or more **A records** (IP addresses). Go back to your domain registrar's DNS settings and replace any existing A records with the ones provided by Firebase.

After updating the DNS records, it may take a few hours for the changes to take effect globally. Once complete, your site will be live at your custom domain with a free, automatically-renewing SSL certificate.

This is the standard and most direct way to publish your site from this environment. You do not need a paid plan to do this.
