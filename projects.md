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

#### Data Handling:
- The component imports `cardData` and `textData` for card images and corresponding text.
- The `calculateVisibleCardArray` function is used to determine which cards should be visible based on the current selected index.

#### State Management:
- The component uses the React `useState` hook to manage the current selected index (`current`) and keeps track of the total number of cards (`length`).

#### Navigation:
- Navigation between cards is handled by the `nextSlide` and `prevSlide` functions, which update the `current` index accordingly.
- Arrow keys (left and right) trigger navigation, and the `handleArrowKey` function is responsible for handling these keyboard events.

#### Keyboard and Mouse Interaction:
- Arrow buttons (`MdKeyboardArrowLeft` and `MdKeyboardArrowRight`) trigger navigation and are styled using the `classnames` library.
- The `handleEnterKey` function handles the Enter key press event, allowing navigation to the next card.
- The container itself is a focusable element (`role="button"`, `tabIndex={0}`) to capture keyboard events.

#### Card Rendering:
- The visible cards are rendered inside the container using the `visibleCards` array.
- Each card is represented as a pair of front and back images, and the classnames are dynamically assigned to achieve a flip effect on the central card (`index === 2`).

#### Text Rendering:
- Text data is rendered based on the current index, and only the active text is displayed.

#### Swipe Gesture:
- The component uses the `framer-motion` library to handle swipe gestures for navigating between cards.
- The `motion.div` with drag properties allows users to swipe left or right to trigger the `prevSlide` or `nextSlide` functions.

#### Accessibility:
- The component includes accessibility features, such as the use of ARIA attributes (`role` and `tabIndex`) to enhance keyboard navigation and screen reader support.

In summary, this React component provides an interactive and visually appealing way to navigate through a set of cards, combining keyboard, mouse, and swipe interactions for a seamless user experience.

### What went wrong / how to improve:

   - The integration of the component into the larger website ended up breaking the animation. I would change how the implementation of the animation ended up since it was not how the original component was developed.
   - Less reliance on regular old DIVs and more descriptive HTML tags

---

## FWGS

### Overview:

Utilizing language models to create a document augmentation application.

1. Extract items from a corpus of text using small, focused language models capable of NER.
2. Utilize a large language model to perform RAG on the RFQ documents.
3. Containerize the application for deployment on customer's hardware
4. Design and develop a front end wrapper for the whole project for a nice user experience.

### What went wrong / how to improve:
