[![etup Shopify Conversion Tracking for [Microsoft Ads]](https://i.ytimg.com/vi/Lv92dhETmMA/maxresdefault.jpg)](https://youtu.be/Lv92dhETmMA?list=PLvT_6E7D1NZIlHa09cgswsjD9QunUpHKy)

Are you running Microsoft Ads for your Shopify store but can’t tell which clicks are turning into customers? Without conversion tracking, you’re essentially flying blind—unable to measure your return on ad spend (ROAS) or optimize your campaigns for real results.

Microsoft Ads (formerly Bing Ads) is a powerful alternative to Google Ads, offering access to a different audience often at a lower cost-per-click. But to make it work, you need to track what matters: **purchases, add-to-carts, and checkouts**.

In this straightforward tutorial, I’ll walk you through how to implement Microsoft Ads conversion tracking on your Shopify store using the UET (Universal Event Tracking) tag. Let’s turn your data into actionable insights.

## Why You Need Microsoft Ads Conversion Tracking ##
Before we dive into the steps, understand what this setup will unlock for your business:

**Measure ROI**: See exactly which ads and keywords are driving sales.
**Optimize Campaigns**: Automatically optimize your bids for conversions.
**Track User Journey**: Understand key events like product views and add-to-carts.
**Leverage a New Audience**: Tap into the Microsoft Audience Network effectively.
## Prerequisites

A live Shopify store.
An active Microsoft Ads account.
Marketing & Analytics permissions in your Shopify admin.
## Step-by-Step Guide: Implementing Microsoft Ads UET Tag on Shopify
Follow these steps carefully to set up your tracking correctly.

# Step 1: Create a UET Tag in Microsoft Ads

Log in to your **Microsoft Advertising account**.
In the top menu, navigate to **Tools > Conversion Tracking**.
Under the “UET tags” section, click the **Create UET tag** button.
Give your tag a descriptive name, like “Shopify Purchase Tracking.”
(Optional) You can choose to enable Microsoft Clarity for user behavior analytics, but for this guide, we’ll focus solely on conversion tracking.
Click **Save and next**.
On the “Install your tag” page, select **Install the tag yourself** and click **Next**, then **Done**.
**Important**: Copy and save the unique **Tag ID** provided on the confirmation page. You will need this in the next step.

# Step 2: Add the Custom Pixel in Your Shopify Admin

From your **Shopify admin dashboard**, go to **Settings > Customer Events.**
Click on **Add custom pixel.**
Name this pixel (e.g., “Microsoft Ads Tracking”) and click **Add pixel.**

# Step 3: Implement the Tracking Code

This is the most critical part. You need to add a specific code snippet to your new pixel.

We will use the official code from Microsoft’s help documentation. You can find the link in the video description or by searching “Shopify Microsoft UET tag setup.”
**Copy the entire code snippet** from the Microsoft help article.
Return to your Shopify admin and **paste the code** into the box for your newly created Microsoft Ads pixel.
Now, find the part of the code that says var tagId = "ENTER_TAG_ID";.
**Replace** ENTER_TAG_ID with the actual **Tag ID** you copied from Microsoft Ads in Step 1. Make sure it’s within the quotation marks.
Your final code should look something like this:
var tagId = "1234567"; // Your actual Tag ID

Click **Save**.

# Step 4: Connect and Test Your Pixel

Back in the **Customer Events** page in Shopify, find your Microsoft Ads pixel and click the **Connect** button.
Once it shows as connected, click the **Test** button.
A new window will open. Now, **browse your store** to fire test events.
Visit your homepage to see a page_view event.
Click on a product to see a product_viewed event.
Add an item to the cart to see an added_to_cart event.
Proceed to checkout to see a checkout_started event.
If you see these events being received in the test panel, congratulations! Your Microsoft Ads conversion tracking is successfully implemented.

# What’s Next?
It can take up to 24-48 hours for data to fully populate in your Microsoft Ads dashboard. After that, you can:

**Create Conversion Goals**: In Microsoft Ads, go to “Conversion Tracking” and create goals for “Purchase” using your UET tag.
**Analyze Performance**: See which campaigns are driving the most valuable customers.
**Use Smart Bidding**: Switch to conversion-focused bid strategies like “Target CPA” to automate your spending.
# Frequently Asked Questions (FAQ)
**Q: How long does it take for conversions to appear in Microsoft Ads?**
A: It can take up to 24 hours for the data to process and appear in your reports.

**Q: Is this method approved by Shopify and Microsoft?**
A: Yes, this method uses Shopify’s native custom pixel functionality and Microsoft’s official UET tag, making it a stable and reliable setup.

**Q: Can I use this for dynamic remarketing?**
A: Absolutely. Once the UET tag is firing correctly, you can set up dynamic remarketing campaigns in Microsoft Ads to re-engage visitors who viewed products but didn’t purchase.

# Conclusion
Setting up Microsoft Ads conversion tracking on Shopify is a straightforward process that unlocks powerful data for your e-commerce business. By following this guide, you’ve taken a crucial step away from guessing and toward data-driven decision-making.

Now you can confidently allocate your budget, knowing which parts of your Microsoft Ads strategy are genuinely profitable.

**Need more Shopify help?** Check out our channel, WebSense Pro, for free tutorials on Shopify UI/UX, custom sections, and web development.
