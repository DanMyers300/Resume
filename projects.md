# Projects

## [Waterloo-Greenway Chatbot](https://waterloogreenway.org/)

### Overview:

- **Objective:** Provide information about park locations to patrons via a conversational bot implemented using AWS services.
- **Technologies Used:**
  - **AWS Lex:** Natural Language Processing for understanding user messages.
  - **AWS Lambda:** Serverless function for handling message processing and interaction.
  - **AWS SNS (Simple Notification Service):** Facilitates communication between components.
  - **AWS Pinpoint:** Enables personalized communication with users via SMS.
  - **AWS CloudWatch:** Monitors application logs and provides notifications for issue detection.
  
### Workflow:

1. **User Interaction:**
   - Patrons send messages to the AWS Pinpoint number.

2. **Trigger Chain:**
   - Pinpoint forwards user messages to SNS.
   - SNS triggers a Lambda function.

3. **Lambda Function:**
   - Written in base JS using Node.js.
   - Utilizes AWS SDK to retrieve and parse user messages from a JSON file.
   - Sends parsed messages to Lex bot using AWS SDK.
   - Receives Lex bot's response.

4. **Response Handling:**
   - Lambda invokes another function to send the Lex bot's response back to Pinpoint using the AWS SDK.

5. **Monitoring:**
   - CloudWatch Logs monitor the Lambda function.
   - CloudWatch alerts and notifications are set up for issue detection and prompt action.

### Example Conversation Flow:

   - User: Requests information about a specific location in the park.
   - Lex Bot: Responds with details.
   - User: Chooses to receive more information or not.

### Notes:

   - Multiple responses are supported for each conversational chain.
   - The system is entirely built using AWS products for seamless integration.
   - CloudWatch Logs provide a centralized monitoring solution with notifications for proactive issue resolution.

### What went wrong / how to improve:

   - Properly researching costs before telling the project manager that something can be done.

---

## [Paleoindian Site](https://paleoindian-site.vercel.app/)

### Overview:

Work in tandem with a senior software developer to create custom React components for use in a educational website for TXDOT.

- **Technologies Used:**
   - **NextJS**
   - **Typescript**
   - **ReactJS**
   - **Framer Motion JS library**

### Components:
   - Card Component
   - Ocean Image flip
   - True / False

---

## [Card Component](https://cards-two-ashy.vercel.app/)

### Overview:

This project is a React component called `Cards` that displays a set of cards with images and text. It allows users to navigate through the cards using arrow keys, mouse clicks on arrow buttons, or swipe gestures. The cards are displayed in a container, and the visible cards are dynamically calculated based on the current selected index.

- **Data Handling:** Imports `cardData` and `textData`, calculates visible cards.
- **State Management:** Uses React `useState` for `current` index and `length`.
- **Navigation:** `nextSlide` and `prevSlide` functions, arrow keys for navigation.
- **Interaction:** Arrow buttons styled with `classnames`, Enter key navigation.
- **Card Rendering:** Dynamic classnames for flip effect on central card.
- **Text Rendering:** Displays text based on the current index.
- **Swipe Gesture:** Utilizes `framer-motion` for left/right navigation gestures.
- **Accessibility:** Includes ARIA attributes for enhanced navigation and screen reader support.


### What went wrong / how to improve:

   - The integration of the component into the larger website ended up breaking the animation. I would change how the implementation of the animation ended up since it was not how the original component was developed.
   - Less reliance on regular old DIVs and more descriptive HTML tags

---

## [Fort Worth Gasket and Supply](https://www.fortworthgasket.com/)

### Overview:



### What went wrong / how to improve:
