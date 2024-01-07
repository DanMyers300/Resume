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
   - Messages sent to AWS Pinpoint.

2. **Trigger Chain:**
   - Pinpoint forwards messages to SNS.
   - SNS triggers a Node.js Lambda function.

3. **Lambda Function:**
   - Parses and sends user messages to Lex bot.
   - Receives Lex bot's response.

4. **Response Handling:**
   - Lambda invokes another function to send Lex bot's response back to Pinpoint.

5. **Monitoring:**
   - CloudWatch Logs monitor Lambda.
   - CloudWatch alerts set up for issue detection.


### Example Conversation Flow:

   - User: Requests information about a specific location in the park.
   - Lex Bot: Responds with details.
   - User: Chooses to receive more information or not.

### Notes:

   - Multiple responses are supported for each conversational chain.
   - The system is entirely built using AWS products for seamless integration.
   - CloudWatch Logs provide a centralized monitoring solution with notifications for proactive issue resolution.

### What went wrong / how to improve:

   - Properly researching costs before telling the project manager that something can be done. I informed the PM early in the project that we could use a shortcode phone number but that ended up being exceedingly expensive and out of budget.
   - Less reliance on a single platform for most of the application, this ended up not allowing the customer to change hosting platforms later when they wanted to

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
