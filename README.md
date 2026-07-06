# Pepperfry-Automation
Objective To automate the Pepperfry guest user journey by validating product browsing, filtering, selection, and cart functionality. Ensure product details like name, price, and availability remain consistent from product page to cart while handling dynamic UI elements.
# User Story – Pepperfry Browse & Cart Validation
Overview A guest user visits the Pepperfry website, navigates through furniture categories, applies filters, selects a product, and validates product details such as name, price, and availability before adding it to the cart. The system must ensure data consistency across listing, product detail, and cart pages.

User journey First, open the Pepperfry homepage and handle any cookie consent or login pop-ups if they appear. Then go to a furniture category like chairs, tables, or sofas. After that, apply a filter such as price range, brand, or category to refine the product list. Once the products are updated, select the first visible product that has a price and open its product details page. From there, add the product to the cart. Next, open the cart page and finally verify that the correct product details like name, price, and quantity are displayed properly in the cart.

Automation Focus Validate navigation from homepage to category page Handle dynamic pop-ups and overlays Apply filters and validate product list updates Capture product details (name, price, availability) Validate product selection from dynamic UI Verify add-to-cart functionality Validate cart content against selected product

Key Validations Correct category page is loaded Filter updates product listing correctly Product name is displayed and consistent Product price is correctly shown (including discounts if any) Product availability/status is visible Same product is added to cart Cart reflects correct product details No mismatch between product page and cart page

Important Considerations Handle dynamic UI elements (lazy loading product cards) Manage pop-ups (cookie consent, login prompts) Avoid hardcoded product values Use explicit waits for product loading and cart updates Handle stale elements during navigation Ensure stable locators for product cards and price elements Manage AJAX-based content updates

Goal Ensure a stable and reliable automation flow that validates the complete Pepperfry guest shopping journey from product discovery to cart verification with accurate data consistency.

# User Flow / Screen Flow
Home -> Login->Product->Cart->End

#Tools & Technologies Used

|Category	        |Tool / Technology|
|-----------------|-----------------|
|Programming       |Language	Java|
|Automation        |Tool	Selenium WebDriver|
|Testing           |Framework	TestNG|
|Browser	          |ChromeDriver|
|Build Tool	      |Maven|
|IDE	              |Eclipse|
|Reporting	        |Extent Spark Reports|
|Logging	          |Log4j|
|Test Data	        |Excel (testdata.xlsx)|
|Configuration	    | config.properties|
|Data Utility	    | ExcelUtils|
|Architecture	    | Hybrid Framework (POM + Data-Driven)|
|Project Structure |	Layered (Pages, Tests, Utils, Resources)|

# FrameWork Structure
<img width="380" height="561" alt="CaptureAutomation" src="https://github.com/user-attachments/assets/d94af9ac-1c21-49b0-b855-ee0aed67248a" />

# Test Strategy
Execution Approach

The automation will follow a modular and parallel development approach to ensure faster execution and maintainability. Each major functionality of the Pepperfry user journey will be automated independently and later integrated into a single end-to-end test flow.

Work Distribution
Member 1: Framework setup & Home test cases
Member 2: Category & Product listing test cases
Member 3: Filter & Product details test cases
Member 4: cart validation ,Documentation & Reporting

#Product detail verification (name, price, availability) Add to cart functionality Cart page validation Integration Plan Each module will be developed and tested independently using Page Object Model (POM) All modules will be integrated into a single end-to-end test suite Final execution will validate full user journey from homepage to cart verification TestNG suite will be used for orchestration and execution control Testing Focus

# Key areas:

Product data consistency across pages Dynamic UI handling Cart accuracy validation Filter correctness Stability of end-to-end flow Execution Priority First: Happy path execution (valid category → product → cart) Next: UI and functional validations (filters, product selection accuracy) Then: Edge cases (no results, slow loading, pop-ups) Final: Full regression execution (complete end-to-end flow)

Data & Synchronization Handling Test data managed using Excel or properties files Explicit waits used for dynamic product loading Handling AJAX-based updates in product listing and cart Avoid hardcoded product names/prices for stability Proper synchronization to handle dynamic DOM changes Outcome

# Test Cases
<img width="824" height="559" alt="CaptureAutomation1" src="https://github.com/user-attachments/assets/f473ab44-40f4-42b5-aecc-647c72aa4a9b" />
