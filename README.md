<p align="center">
  <img src="https://avatars.githubusercontent.com/u/90627799?s=400&u=fd374a5ad98b79d429b4177bea59f0db9f7ca71a" alt="code-ssh logo" width="200"/>
</p>

<h1 align="center">Welcome To Weframe's Medusa Classroom</h1>

In this documentation, you'll find how-to guides and tutorials that will help you customize the Medusa server and admin. These guides are useful after you've learned Medusa's main concepts in the [Get Started](https://docs.medusajs.com/learn) section of the documentation.

## Medusa How-To Tutorials

- [Create Auth Provider](https://docs.medusajs.com/resources/references/auth/provider)
  - [Create Cache Module](https://docs.medusajs.com/resources/architectural-modules/cache/create)
- [Use Cache Module](https://docs.medusajs.com/resources/references/cache-service)
  - [Create Event Module](https://docs.medusajs.com/resources/architectural-modules/event/create)
- [Use Event Module](https://docs.medusajs.com/resources/references/event-service)
- [Create Fulfillment Provider](https://docs.medusajs.com/resources/references/fulfillment/provider)
- [Create Notification Provider](https://docs.medusajs.com/resources/references/notification-provider-module)
  - [Use Notification Module](https://docs.medusajs.com/resources/references/notification-service)
  - [Send Notification](https://docs.medusajs.com/resources/architectural-modules/notification/send-notification)
- [Create Payment Provider](https://docs.medusajs.com/resources/references/payment/provider)
- [Handle Password Reset Event](https://docs.medusajs.com/resources/commerce-modules/auth/reset-password)
- [Use File Module](https://docs.medusajs.com/resources/references/file-service)
- [Use Workflow Engine Module](https://docs.medusajs.com/resources/architectural-modules/workflow-engine/how-to-use)

### Extend Modules

- [Extend Cart](https://docs.medusajs.com/resources/commerce-modules/cart/extend)
- [Extend Customer](https://docs.medusajs.com/resources/commerce-modules/customer/extend)
- [Extend Product](https://docs.medusajs.com/resources/commerce-modules/product/extend)

### Admin

- [Components & Layouts\*\*](https://docs.medusajs.com/resources/admin-components)

### Deployment Guides

Deployment guides are a collection of guides that help you deploy your Medusa server and admin to different platforms. Learn more in the [Deployment Overview](https://docs.medusajs.com/resources/deployment) documentation.

---

# Project Overview: **Medusa Store Platform (Weframe Classroom Tasks)**

A mock project: **"Weframe Gear Shop"** — an online store selling digital and physical products. Each task adds a new capability to the store, starting with foundational setup and leading to deeper customizations.

### **⚙️ Module 1**

> Goal: Get familiar with Medusa’s setup and how to extend core features.

---

#### 1. **Project Setup**

- [ ] Setup Medusa project using [`create-medusa-app`](https://docs.medusajs.com/resources/create-medusa-app). Do keep in mind that your db is not running locally, means you guys have to provide your db url with above create command.
- [ ] Configure PostgreSQL and Redis
- [ ] Setup Medusa Admin Panel

#### 2. **Extend Core Modules**

- [ ] Extend **Cart** to support a custom discount rule (e.g. “Buy X Get Y”)
- [ ] Extend **Customer** to include additional fields like birthday or loyalty tier
- [ ] Extend **Product** to support custom metadata like license key type (for digital products)

### **⚙️ Module 2**

> Goal: Understand how to create and use custom architectural modules.

---

#### 3. **Authentication**

- [ ] Create a **Custom Auth Provider** (e.g., magic link or social login)
- [ ] Handle **Password Reset Event** with custom email content

#### 4. **Cache & Event Handling**

- [ ] Create **Cache Module** to cache product availability checks
- [ ] Use **Cache Service** in a product availability controller
- [ ] Create **Event Module** to track custom events (e.g., wishlist added)
- [ ] Use **Event Service** to emit and listen to `wishlist.created` or `cart.abandoned` events

#### 5. **File Service**

- [ ] Use **File Module** to allow uploading product instruction PDFs or marketing images

### **⚙️ Module 3**

> Goal: Learn how to integrate external systems and build real-world scalable workflows.

---

#### 6. **Fulfillment & Payment Providers**

- [ ] Create a **Custom Fulfillment Provider** for local courier delivery
- [ ] Create a **Custom Payment Provider** using a mock gateway (or Razorpay/Stripe if available)

#### 7. **Notification System**

- [ ] Create **Notification Provider** (e.g., Email via SendGrid, WhatsApp via Twilio)
- [ ] Use **Notification Service** in various flows (order confirmation, password reset)
- [ ] Trigger **Send Notification** on order completion

#### 8. **Workflow Engine**

- [ ] Use the **Workflow Engine** for an advanced flow:
  - Order placed → Stock checked → Payment captured → Fulfillment started → Notification sent

### **⚙️ Module 4**

> These are ideal for those who also want to customize the Medusa Admin Panel.

---

#### 9. **Admin UI Customization**

- [ ] Learn about **Admin Components & Layouts**
- [ ] Create a new page in Admin for managing custom workflows or support tickets
- [ ] Add custom tab in product edit view for managing digital product metadata

### **⚙️ Module 5**

> Expose your local development.

In this module, you’ll learn how to expose your local Medusa server and Admin to reviewers using `ngrok`. You are **not required** to deploy to any cloud provider.

2. **Start Medusa Server and Admin Locally**

   - Run your Medusa backend and admin locally as usual.

3. **Install ngrok**

   - [Official ngrok install](https://ngrok.com/downloads/mac-os)

4. **Expose Your Local Server with ngrok**

   - Start ngrok on the port your Medusa backend is running (default: `9000`)

   ```bash
   ngrok http 9000
   ```

   - For Storefront you have to expose port 3000.

   ```bash
   ngrok http 3000
   ```

5. **Share the URLs**
   - Once ngrok provides you public URLs, share them with the review team.
   - Ensure that both the Medusa server and Admin are accessible.

## 📝 Bonus Ideas

- Implement multi-vendor support with custom APIs
- Build a dashboard using the Notification & Event logs
- Add support for different sales channels (B2B, DTC)
- Integrate analytics by emitting events to a service like Segment or Plausible

# Code Submission Guidelines

1. **Clone the Repository**  
   Ensure you have the latest version of the codebase by pulling the most recent changes:

   ```bash
   git pull origin main
   ```

2. **Create a New Branch**  
   Create a new branch using the following naming convention:

   ```bash
   git checkout -b code.<your-github-username>
   ```

3. **Push Your Changes**

   - Make sure your code is clean, well-documented, and passes any existing checks or linters before submitting
   - After completing your development work, push your changes to your feature branch:

   ```bash
   git push origin code.<your-github-username>
   ```

4. **Open a Pull Request**

   - Navigate to the repository on GitHub.
   - Create a new pull request with `code` as the base branch.
   - Add a clear title and description summarizing your changes.

5. **Notify the Team**  
   Once your pull request is created, notify the team in the group chat for review and feedback.
