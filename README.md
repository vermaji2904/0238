# 🌐 **Guide to Deploying a Next.js Project to Expo**

## 🚀 **Steps to Deploy Using Expo CLI**

### 1️⃣ **Configure Your Next.js Project**

- Update `next.config.ts` to enable static export:

  ```typescript
  import type { NextConfig } from "next";

  const nextConfig: NextConfig = {
    output: "export",
    reactStrictMode: true,
  };

  export default nextConfig;
  ```

### 2️⃣ **Build the Project**

Run the following command to generate the output files:

```bash
npx next build
```

### 3️⃣ **Deploy with Expo**

Use Expo Application Services (EAS) to deploy your project:

```bash
eas deploy --export-dir=out
```

### 4️⃣ **Get Your Deployment URL**

- After deployment, you’ll receive a link to access your project:
  ```
  https://bhuvneshverma--yxdct6yk0b.expo.app
  ```

### 5️⃣ **Switch to Production (Optional)**

- To set up a production alias, use:
  ```bash
  eas deploy:alias --prod --id=DEPLOYMENT-ID
  ```
  Example:
  ```bash
  eas deploy:alias --prod --id=yxdct6yk0b
  ```

### 🎯 **Final Production URL**

Once deployed to production, your project url will look like :  
`https://bhuvneshverma.expo.app`

🔗 **Check it out:**

[![Bhuvnesh Verma](bhuvneshverma.expo.app.png)](https://bhuvneshverma.expo.app)

### 💡 **Acknowledgments**

Special thanks to [ide](https://github.com/ide) for their clear and concise explanation regarding the deployment of Next.js projects using Expo Application Services (EAS).
