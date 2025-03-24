# Open WebUI

## Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/Frzk/openwebui my-openwebui
   cd my-openwebui
   ```

2. Create an app:
   ```bash
   scalingo create my-openwebui
   ```
   This adds a `scalingo` remote to your repository.

3. Attach a PostgreSQL addon:
   ```bash
   scalingo --app my-openwebui addons-add postgresql postgresql-starter-512
   ```

4. Push to Scalingo:
   ```bash
   git push scalingo master
   ```
   **This first deployment** is expected to fail: the resulting image is very
   big, even with the use of the `.slugignore` file.

> [!IMPORTANT]
> Please get in touch with our support team to increase the size of your
  application image to 3GB.

5. Once our support team has increased the size of your application image,
   trigger a new deployment:
   ```bash
   git push scalingo master
   ```
   This time the deployment should be successful.

