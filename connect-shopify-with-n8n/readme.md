[![Connect Shopify with N8N Updated – 2026 – AI Automation
](https://i.ytimg.com/vi/B-Zi735UdeY/maxresdefault.jpg)](https://youtu.be/B-Zi735UdeY?list=PLvT_6E7D1NZIlHa09cgswsjD9QunUpHKy)

If you have tried connecting N8N to Shopify recently and got hit with an error you are not alone.

For years, the “Access Token” method was the go-to solution. You would create a custom app in Shopify, grab a token, paste it into N8N, and boom—automation worked.

But as of January 1st, 2026, Shopify no longer allows merchants to create legacy custom apps using the old method.

The good news? The fix is actually simple. You just need to switch to OAuth. And honestly? It is a cleaner, more secure way to connect.

Here is exactly how to do it step by step.

Why This is Happening
Shopify is pushing developers and store owners toward the Dev Dashboard and Shopify CLI. The old “Develop apps” section inside your Shopify admin is gone for new installations.

If you try to use the old Access Token method in N8N today, you will hit a wall. OAuth is now the only way.

Let us fix your connection.

What You Will Need
An N8N instance (self-hosted or cloud)
A Shopify store (development or live)
10 minutes of focus
## Step 1: 

# Start Fresh in N8N
Open your N8N workflow.

Add the Shopify node.
Choose your operation (e.g., “Get Many Products”).
In the Credential dropdown, click “Create New”.
Select “OAuth2” as the authentication method.
Do not look for the Access Token option—it is no longer relevant.

## Step 2:

# Create a New App in Shopify Dev Dashboard
This is the step most people get stuck on. But it is easier than it sounds.

Log in to your Shopify admin.
Click on your profile icon (top right) and select “Dev Dashboard”.
If you do not see this, you may need to create a free Shopify Partners account first.
Click “Create App”.
Give your app a name (e.g., “N8N Connection”).
Choose “Custom App” and click Create.

## Step 3:

# Configure Access Scopes (Be Careful Here!)
This is the security part.

Scroll down to “Scopes” and click “Select Scopes”.
Search for the data you want to pull.
Products → Select all product scopes.
Orders → Search and select order scopes.
Customers → Search and select customer scopes.
Do not select everything. Only pick what N8N actually needs. This keeps your store safe.
Click “Done”.
## Step 4:

# Add the Redirect URL
This is the glue between N8N and Shopify.

Go back to your N8N credential creation window.
Find the “OAuth Redirect URL” field.
Click “Click to copy” (it looks like https://your-n8n.com/rest/oauth2-credential/callback).
Go back to your Shopify app settings.
Paste the URL into “Allowed redirection URL(s)”.
Click “Save” and then “Release”.


## Step 5:

# Install the App

Now it is time to connect the dots.

In your Shopify Dev Dashboard, go to the “Overview” tab of your app.
Click “Install App”.
You will see a permission screen. Click “Install”.
Once installed, you will land on an example app page. That is fine.
## Step 6:

# Copy Credentials to N8N

In your Shopify app settings, locate your Client ID and Client Secret.
Copy both.
Paste them into the N8N credential window.
Now find your Shop Subdomain.
Look at your Shopify URL: https://**your-shop-name**.myshopify.com
Copy only the your-shop-name part.
Paste it into the “Shop Subdomain” field in N8N.
Click “Save”.
## Step 7:

# Connect and Test

Click “Connect My Account”.

N8N will ask you to log in to Shopify (if you are not already) and confirm the permissions.

Once authorized, close the pop-up window.

Now hit “Execute Step” in N8N.

If everything is set up correctly, your Shopify product data will appear instantly.

## Final Thoughts

I will be honest when I first saw Shopify remove the legacy app access, I was frustrated. It felt like an unnecessary roadblock.

But after switching to OAuth, I actually prefer it. It is more transparent. I know exactly what scopes my automation has, and I do not have to worry about long-lived tokens sitting around.

If you are coming from an old video or an old workflow, I hope this guide saved you some time.
