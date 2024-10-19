# Capitol_AI_Zombie
Zombie Armband ID
This project involves developing an object recognition system that can detect both humans and zombies during Zombie Week, based on their armbands. Upon detection, the system will change the colors of Philips Hue LEDs in the room to indicate their respective presences. The system will use YOLOv11 as the backend, with training data generated via Label Studio. LED control will be managed through API calls to Philips Hue bridges.

This project serves as an educational experience for participants, offering opportunities to learn and apply skills such as using Git, fine-tuning object detection models, and making API calls. It also aims to spark interest in AI among students visiting the AICE (Artificial Intelligence Center of Excellence), encouraging them to get involved in future projects.


Design and Implementation Strategy for the Object Recognition System
1. Project Planning & Requirements Gathering

    Define Objectives: Clearly outline the system’s purpose (detecting humans and zombies based on armbands, changing LEDs based on detection).
    Identify Hardware & Software:
        Hardware: Cameras for input, Philips Hue lights for output.
        Software: YOLOv11 for object detection, Label Studio for dataset tagging, Philips Hue API for controlling LEDs.
    Team Roles: Assign roles (project manager, data scientist, developer, API integrator, etc.) based on expertise.

2. Data Collection & Labeling

    Image Dataset Creation:
        Collect images of humans and zombies with identifiable armbands.
        Ensure diversity in angles, lighting, and conditions.
    Annotation:
        Use Label Studio to label the dataset (identify and tag armbands on both humans and zombies).
    Data Augmentation: Apply transformations (rotation, brightness, scaling) to increase dataset diversity.

3. Model Selection & Training

    YOLOv11 Customization:
        Pre-train or fine-tune YOLOv11 on the labeled dataset from Label Studio.
        Customize YOLOv11 configuration (e.g., model architecture, anchor boxes) for optimal detection of armbands.
    Model Validation:
        Split the dataset into training, validation, and test sets.
        Train the model, iterating with hyperparameter tuning to improve detection accuracy.
        Evaluate the model’s performance using metrics like precision, recall, and mAP (mean average precision).

4. API Integration for LED Control

    Philips Hue API:
        Explore and understand the API documentation for the Hue Bridge.
        Develop API calls to control LED lights based on object detection results.
        Establish color-coding logic for LED responses:
            Red for zombies.
            Green for humans.
    Testing API Integration:
        Test calling the Hue API in isolation to ensure reliable communication and proper LED response.

5. System Architecture Design

    Input Pipeline:
        Set up a camera feed to continuously capture images in real-time.
        Use the YOLOv11 model to process the video stream and detect objects (humans and zombies).
    Decision Logic:
        Based on the detection (human/zombie armbands), trigger the appropriate API call to change LED colors.
    Edge Computing (Optional):
        Implement on-device inference to reduce latency if real-time processing is required.
        Optimize the system for speed if hardware constraints exist.

6. Implementation Phases

    Phase 1: Prototype Object Detection
        Implement basic object detection using pre-labeled data.
        Test detection accuracy and improve it through fine-tuning.
    Phase 2: API Integration
        Integrate the system with the Philips Hue API and test the lighting controls based on detection.
    Phase 3: End-to-End Testing
        Test the entire system (video feed -> object detection -> LED control) in real-world conditions (Zombie Week).
    Phase 4: Optimization
        Identify bottlenecks (e.g., processing time, detection accuracy).
        Refine model or code for performance improvements.

7. Educational Focus

    Document Processes:
        Maintain clear documentation for each part of the project (from data collection to model deployment and API calls).
        Include tutorials on Git usage, object detection, and API development for team members.
    Team Collaboration:
        Use GitHub for version control and collaboration.
        Encourage code reviews, commit best practices, and continuous integration.

8. Deployment & Demo

    System Deployment:
        Deploy the object detection system on the target hardware.
        Ensure the Philips Hue lights and camera feeds are correctly set up in the Zombie Week room.
    Live Demo:
        Prepare for a live demo during Zombie Week to showcase the system’s functionality.
        Plan for contingency, such as backup power, redundant cameras, and quick fixes for LED malfunctions.

9. Post-Project Analysis

    Performance Evaluation:
        Analyze the model’s real-world performance during Zombie Week.
        Collect feedback from team members and students to assess learning outcomes.
    Future Improvements:
        Explore more sophisticated models or additional features (e.g., audio cues, expanded detection to include other objects).
        Plan for scaling the project or applying it to new use cases.

By following this approach, you'll build a structured roadmap that allows for methodical development while keeping educational value at the forefront.


#Next Project (Thinking Bigger)
Object Detection Applied to Real World

1. Project could relate to Ukraine armbands. Soldiers wear yellow armbands in Ukraine to be detected by drones flying overhead in order for the drones
to not attack friendlies.
2. Project could include recognizing medical teams/doctors on the battlefield. Drones that fly overhead will know not to attack recognized non-combatants
or deliver packages to those invidividuals.
