## Text to image with AI 

[SITE](https://ai-text2image-sxidsvit.vercel.app/)


### Core Application Idea 

The service provides an API for generating images based on text descriptions.<br/> 
The API route /api/image/generate-image leverages the capabilities of the [Clipdrop API](https://clipdrop.co/apis/docs/text-to-image) to convert text into images. <br/>
The service features an intuitive web interface for user convenience.

---

![]()
<img src="demo.gif" alt="Table" width="600" height="450" style="display: block; margin-left:100px ;"> 

---

### Basic features
#### 1. Frontend (client part):
- Based on React.js using React Router for routing.
- Uses Tailwind CSS for styling.
- Uses Clipdrop API to convert text into images.
- AXIOS is used to send HTTP requests.
- Designed with the Vite Collector, which speeds up development and improves performance.

#### 2. Backend (server part):
- Works on Node.js using Express.
- For data storage MongoDB is used.
- Integration with Razorpay and Stripe payment systems to provide paid services (for example, adding credits for image processing).
- Authentication and authorization are performed via JSON Web Token.
- Integration of a third-party API for image processing (e.g., CLIPDROP API).


#### 3. Main API routes:

##### 3.1 User Router:
- Register user & login user.
- Processing payments via Razorpay and Stripe.
- Check user credit.

``` js 
userRouter.post('/register', registerUser)
userRouter.post('/login', loginUser)
userRouter.get('/credits', authUser, userCredits)
userRouter.post('/pay-razor', authUser, paymentRazorpay)
userRouter.post('/verify-razor', verifyRazorpay)
userRouter.post('/pay-stripe', authUser, paymentStripe)
userRouter.post('/verify-stripe', authUser, verifyStripe)
```

##### 3.2 Text to Image Router:
- text to image generate via /api/image/generate-image API.

``` js 
imageRouter.post('/generate-image', authUser, generateImage)
```

<img src="api-testing.jpg" alt="API testing" width="900" height="400" style="display: block; margin-left:0px ;">
---


#### 4. Configuration via . env:

- Environment variables contain API keys and configuration settings for the client and server.

``` js 
Client: 
VITE_BACKEND_URL = 
VITE_RAZORPAY_KEY_ID = 

Server: 
JWT_SECRET =
MONGODB_URI = 
CLIPDROP_API = 
CURRENCY =
RAZORPAY_KEY_ID = 
RAZORPAY_KEY_SECRET = 
STRIPE_SECRET_KEY=
```

---

### Tech Stack

- Client:  React.js 18,  React Router 6,  Tailwind CSS, Clipdrop,  AXIOS,  VITE

- Server: NODE,  EXPRESS,  MONGODB,  AXIOS, CLIPDROP,  RAZORPAY,  STRIPE, JSON WEB TOKEN,  FORM DATA, BCRYPT

<img src="db-tables.jpg" alt="Table" width="450" height="300" style="display: block; margin-left:100px ;">

---


##### Contact with me:

[<img alt="webDev | LinkedIn" src="https://img.shields.io/badge/linkedin-0077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />][linkedin]

[linkedin]: https://www.linkedin.com/in/sergiy-antonyuk/


##### I can't express how much I have learned from [you](https://www.youtube.com/@GreatStackDev) ! <br> Thanks for the hard and smart work.
