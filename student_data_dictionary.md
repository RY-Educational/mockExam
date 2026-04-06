# BTC1895H  Final Exam Dataset
## Student Data Dictionary

You are given **three CSV files**. Read them carefully before building your model.

## Prediction task

Your goal is to predict:

- **`purchased_next_30d`** in `outcomes_train.csv`

This is a **customer-level prediction task**.

---

# 1. `customers.csv`

One row per customer.

| Column | Description |
|---|---|
| `customer_id` | Unique customer identifier |
| `household_id` | Household identifier; multiple customers may belong to the same household |
| `age` | Customer age in years |
| `gender` | Customer gender code |
| `region` | Customer region label |
| `income_band` | Approximate income category |
| `signup_channel` | Main channel where the customer signed up |
| `signup_date` | Date the customer signed up |
| `membership_tier` | Membership tier/category |
| `account_status_code` | Current account status code |
| `support_case_count_90d` | Number of support cases in the last 90 days |
| `days_since_last_login` | Days since the customer's last login |
| `preferred_device` | Main device used by the customer |
| `marketing_segment` | Internal marketing segment label |
| `record_version` | Internal record version number |

---

# 2. `activity_log.csv`

Multiple rows per customer.  
Each row represents a customer activity event.

| Column | Description |
|---|---|
| `activity_id` | Unique activity/event identifier |
| `customer_id` | Customer identifier |
| `activity_date` | Date of the activity |
| `session_length_min` | Session length in minutes |
| `pages_viewed` | Number of pages viewed in the session |
| `cart_additions` | Number of cart additions during the event/session |
| `promo_clicked` | Whether a promotion was clicked |
| `coupon_shown` | Whether a coupon was shown |
| `coupon_redeemed` | Whether a coupon was redeemed |
| `support_chat_started` | Whether support chat was started |
| `refund_requested` | Whether a refund was requested |
| `shipping_delay_flag` | Whether shipping delay was flagged |
| `device_type` | Device type used during the event |
| `campaign_id` | Marketing campaign identifier |
| `event_source` | Event source/channel |
| `event_batch_id` | Internal event batch identifier |

---

# 3. `outcomes_train.csv`

One row per customer.  
Contains the target and several related outcome fields.

| Column | Description |
|---|---|
| `customer_id` | Customer identifier |
| `purchased_next_30d` | **Target variable**: whether the customer purchased in the next 30 days |
| `days_to_next_purchase` | Number of days until the next purchase |
| `post_window_spend` | Spend amount recorded after the target window |
| `next_month_loyalty_points` | Loyalty points recorded in the following month |
| `target_snapshot_date` | Snapshot date used to define the target window |

---

# Notes for students

- This is a **customer-level** modeling problem.
- `activity_log.csv` is an **event-level** table.
- Your submission should include:
  - your data preparation,
  - your modeling approach,
  - your metrics,
  - and your reasoning.
- Clear explanation matters as much as code.
