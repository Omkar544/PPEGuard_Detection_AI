This project introduces a robust, real-time solution for automated monitoring and enforcement of Personal Protective Equipment (PPE) regulations within dynamic industrial environments. Leveraging advanced Computer Vision and the YOLOv8 object detection architecture, the system instantly analyzes live video streams (at $\ge 30$ FPS) from surveillance cameras. It is meticulously trained on a custom dataset to identify workers and classify the presence or absence of all required PPE components: safety helmets, gloves, specialized dress code (e.g., safety vests), and safety shoes. Designed for low-latency operation via edge computing, the core function is not just detection, but active compliance verification.The system significantly enhances safety protocols by replacing manual inspection with continuous, automated surveillance. Utilizing integrated object tracking, the platform maintains the identity of individual workers and, upon detecting any non-compliance (e.g., missing gloves), it immediately triggers an instantaneous alert to safety personnel, accompanied by a timestamp and visual evidence. This capability allows for rapid intervention, drastically reducing the risk of workplace accidents, improving overall regulatory adherence, and generating comprehensive compliance reports for auditing purposes.
PPEGuard.AI
├───backend
│   ├───app
│   │   ├───controllers      # Detection and API logic
│   │   ├───models           # Database models (PostgreSQL)
│   │   ├───services         # Detection & classification services
│   │   ├───schemas          # Pydantic schemas
│   │   └───main.py          # FastAPI entrypoint
├───frontend
│   ├───templates            # HTML templates for dashboard
│   ├───static
│   │   ├───css              # Tailwind CSS files
│   │   └───js               # Optional JS files
├───data
│   ├───train
│   ├───valid
│   └───test
├───models
│   ├───yolov8n.pt           # Pre-trained YOLOv8 model
│   └───best.pt              # Custom trained model
├───output
├───results
│   ├───confusion_matrix.png
│   ├───PR_curve.png
│   └───batch_visualizations
