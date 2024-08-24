# StockSavvy

**StockSavvy** is an advanced stock prediction system that utilizes TensorFlow and reinforcement learning techniques to forecast stock prices. This project integrates with the `yfinance` library to fetch historical stock data and includes a Django app that can be seamlessly added to existing Django projects.

## Features

- **Reinforcement Learning Model**: Implements reinforcement learning algorithms for stock price prediction.
- **TensorFlow Integration**: Utilizes TensorFlow for building and training neural networks.
- **Stock Data Retrieval**: Fetches historical and real-time stock data using the `yfinance` library.
- **Django Integration**: Provides a Django app that integrates with existing Django projects for easy deployment and management.

## Libraries and Tools Used

- **TensorFlow**: For constructing and training reinforcement learning models.
- **yfinance**: To obtain stock market data.
- **NumPy**: For numerical computations and data manipulation.
- **Pandas**: For data processing and analysis.
- **Matplotlib**: For plotting and visualizing data.
- **Scikit-learn**: for additional machine learning tools.
- **Django**: For web framework integration.

## Setup and Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/garbhitsh/StockSavvy.git
    cd StockSavvy
    ```

2. **Create and Activate a Virtual Environment:**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Required Packages:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Setup Google Cloud Vision (if applicable):**
   - Follow the [Google Cloud Vision documentation](https://cloud.google.com/vision/docs/quickstart) to set up authentication and obtain your API key.
   - Set up the environment variable for authentication:

     ```bash
     export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/credentials.json"
     ```

5. **Run the Django App (if integrating):**

    ```bash
    python manage.py runserver
    ```



 **Django Integration:**

   - Add the StockSavvy app to your Django project’s `INSTALLED_APPS` in `settings.py`:

     ```python
     INSTALLED_APPS = [
         # Other apps
         'stock_savvy',
     ]
     ```

   - Include the app’s URLs in your project’s `urls.py`:

     ```python
     from django.urls import path, include

     urlpatterns = [
         path('stock/', include('stock_savvy.urls')),
     ]
     ```

   - Configure any required settings in your Django project’s `settings.py` file.

## Configuration

- **Configuration File:** Update the `config.json` file with paths, settings, and API keys as needed.
- **Environment Variables:** Ensure any required environment variables (e.g., API keys) are properly set if applicable.

## Contributing

Contributions are welcome! If you have suggestions, improvements, or issues, please open an issue or submit a pull request. Make sure your contributions align with the project’s guidelines.

## License

This project is licensed under the MIT License. 


