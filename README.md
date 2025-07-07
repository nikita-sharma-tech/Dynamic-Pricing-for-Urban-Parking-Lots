### Dynamic Pricing for Urban Parking Lots
This project implements a real-time dynamic pricing system for 14 urban parking lots using streaming data, economic principles, and ML-style logic — built using Pandas, NumPy, and Bokeh.

📌 Capstone Project for Summer Analytics 2025
Hosted by: Consulting & Analytics Club × Pathway

📁 Dataset
The dataset contains parking lot data for 73 days, sampled every 30 minutes. It includes:

ID: Lot ID

Capacity, Occupancy, QueueLength

TrafficConditionNearby, IsSpecialDay

VehicleType: car, bike, or truck

LastUpdatedDate, LastUpdatedTime: timestamps

🎯 Objective
Build a dynamic pricing model that:

Starts from a base price of $10

Adjusts in real time based on:

Occupancy rate

Queue length

Traffic conditions

Special day flag

Vehicle type

Competitor prices

Ensures price variations are smooth and explainable

🧠 Models Implemented
✅ Model 1: Linear Baseline
python
Copy
Edit
price = previous_price + α × (Occupancy / Capacity)
✅ Model 2: Demand-Based
python
Copy
Edit
Demand = α × (Occupancy / Capacity) + β × QueueLength − γ × Traffic + δ × IsSpecialDay + ε × VehicleTypeWeight
Price is scaled with:

python
Copy
Edit
price = Base × (1 + λ × normalized_demand)
✅ Model 3: Competitive Pricing
Simulates 3 competitor lots

Increases or decreases price based on:

Nearby competitor prices

Utilization levels

🔁 Streaming Simulation
To simulate real-time behavior:

Rows are processed one-by-one with a small delay

Price is computed for each timestamp and lot

Prices are stored in price_log list

📊 Visualization
Real-time pricing graph built with Bokeh

Users can visualize prices for any lot_id

Timestamps shown on X-axis, price on Y-axis

✅ How to Run in Google Colab
Upload your dataset.csv to Colab

Install Bokeh:

bash
Copy
Edit
!pip install bokeh
Run the notebook (includes:

Preprocessing

Pricing loop

Bokeh visualization)

🛠 Future Improvements
Rerouting suggestions to nearby lots if current one is full

Integration with Pathway for real-time pipelines

More realistic competitor pricing (geo-aware)

Multi-lot visualization dashboard (tabs or sliders)

📂 Output
price_log: contains real-time prices

Final graph: pricing trend for selected lot_id

📌 Authors
👩‍💻 Nikita Sharma

🧠 Summer Analytics 2025 Team

💡 Mentor: Consulting & Analytics Club, IITG
