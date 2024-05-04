# image_processing_projection
Graph Academy Project Projection

## Key Features

### Image Upload
- **Users can upload images from their local device.**
- **Users can preview their uploaded images.**

### Background Removal
- **Remove the background while retaining the human figure in the uploaded image.**

### Text Wrapping
- **Wraps text around the boundary of the retained human figure.**

### View Previous Work
- **Users can view and download their previously processed images.**

## Architecture Overview

### Components
- **Client-side, Next.js server, Supabase, and Adobe Photoshop.**

### Workflow
- **Authentication Workflow:** 
  - The client sends authentication data to the Next.js server, which verifies it with Supabase and returns the authentication status to the client.
- **Image Upload and Processing Workflow:**
  - The client uploads an image which is sent to the Next.js server. The server calls the Adobe Photoshop API to handle the processing. The processed result is stored in Supabase and sent back to the client.
- **View Previous Submissions Workflow:**
  - To view previous submissions, the client sends a request to the Next.js server. The server retrieves all previously processed images for that user from Supabase and sends them back to the client side.

## Technology Used

### Client Side: React.js
- **React.js** is very useful for responsive design. Its infinite scroll feature is also useful for displaying all previous submissions.

### Adobe Photoshop API
- **Adobe Photoshop API** is specifically designed for image manipulation. It uses AI/ML-based cloud technology to easily remove subjects from backgrounds (for the background removal part) and can automate entire workflows using Photoshop actions in the cloud (for the text wrapping part).

### Next.js
- Offers flexibility in rendering strategies to optimize performance and SEO. Its integrated API routes simplify the handling of server-side logic and backend functionalities.

### Supabase
- Open source and free to use, compared to Firebase, with easier setup and management of backend services. It supports real-time capabilities and ensures scalability with less overhead.

## Frontend Client
- **React.js Components:**
  - Image upload button
  - Image upload preview
  - Image receive preview
  - Image receive download
  - View previous image functionality

## Next.js Server Functions
- **authenticate_user**
- **image_upload_retrieval**
- **receive_image_upload**
- **request_background_removal**
- **request_text_wrapping**
- **send_back_processed_image**
- **view_previous_work**
