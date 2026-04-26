# S3 Static Website Hosting - Full Steps

## Step 1: Create a Bucket

1. Go to AWS Console -> S3 -> Create bucket.
2. Bucket name (must be unique): `your-site-name`.
3. Select region (example: Mumbai `ap-south-1`).
4. For now, keep Block Public Access disabled (unchecked) so website hosting can work.
5. Click Create bucket.

## Step 2: Upload Files

1. Open your bucket -> Objects tab -> Upload.
2. Upload these files:
   - `index.html` (mandatory)
   - `style.css`
   - `script.js`
   - Images (if any)
3. Click Upload.

## Step 3: Enable Static Website Hosting

1. Open your bucket -> Properties tab.
2. Scroll to Static website hosting.
3. Click Enable.
4. Hosting type: Host a static website.
5. Index document: `index.html`.
6. Error document: `error.html` (optional).
7. Click Save changes.

## Step 4: Enable Public Access

1. Go to Permissions tab.
2. In Block Public Access settings, uncheck Block all public access.
3. Save changes.

## Step 5: Add Bucket Policy (Important)

1. Go to Permissions -> Bucket Policy.
2. Paste this policy and replace the bucket name:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
```

3. Replace `YOUR_BUCKET_NAME` with your actual bucket name.
4. Click Save policy.

## Step 6: Get Static Website URL

1. Go to Bucket -> Properties -> Static website hosting.
2. You will see a URL like:

```text
http://your-site-name.s3-website-ap-south-1.amazonaws.com
```

3. This is your live website link.

## Quick Checklist

- Bucket created
- Files uploaded
- Static hosting enabled
- Public access allowed
- Bucket policy added
- Website URL tested
