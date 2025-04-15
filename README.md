# A. Overview of the Application
Our application is built to enhance the cooking experience by streamlining how users access and follow digital recipes on their mobile devices. It eliminates the distractions commonly found in traditional cooking blogs, such as intrusive ads, unnecessary text, and poor formatting—and instead offers a clean, intuitive interface focused on usability. The app features hands-free voice navigation, allowing users to move through recipe steps without touching their device, along with personalized recipe recommendations based on user preferences. A saved recipes section ensures quick access to favorites, making it easier to return to the dishes you love. Whether you’re a beginner or a home-cooking enthusiast, the app provides a distraction-free and practical way to cook with confidence.

---------------------------------------------------------------

# B. How to Run the Voice Command Code (installation steps, commands)

---------------------------------------------------------------
## Wake Word API Installation Steps
> **Note:** The API used in this project allows only one access key per device.
1. Visit https://picovoice.ai/ and create an account
2. After logging in, copy your **personal access key.** You’ll use this in Step 8
3. After collecting your access key, scroll down to where it says **'Start Building'** and click **'Wake Word'**
4. Under the language section select **'English'**
5. Under Wake Word section type **'Hey Food'**
6. Click the **'Train'** button: a **.ppn file** will be generated and download on your device
7. Add the downloaded .ppn file into the **assets folder** of this project
8. In the **RecipeSteps.java**, locate the **initPorcupine()** method and 
    - Replace the current value in **.setAccessKey()** with **your access key**
    - Replace the current value in **.setKeywordPath()** with the name of your **.ppn file from the assets folder.**
9. Build and run the app on your Android device — voice control is now enabled!

## Voice Commands
After the wake word **"Hey Food"** is detected, you can issue the following commands:
1. "Hey Food" → **"Next"**
    - Moves to the next step in the recipe.
3. "Hey Food" → **"Back"**
    - Returns to the previous step in the recipe.
4. "Hey Food" → **"I am done"**
    - Ends the session and navigates to the performance screen, which shows:
      - **Time Taken**
      - **Battery Usage**
      - **Error Count**
