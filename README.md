# 4G_transition_predict
This project is based on the Data records of customer usage characteristics for 10 consecutive months in a Telecom Company to Predict model of service upgrade to 4G transition 

## **Introduction**

**Dataset**
These include the following main fields:

cuoc_goc_gprs_220601: Customer data revenue generated when using exceeding the allowed traffic
ha_tang_220601: The infrastructure used by KH 2G-3G is an old technology, 4G is a new technology in the future
is_sim_4g_220601: Customers who already have a 4G SIM SIM (Necessary condition for TB to be able to move to 4G infrastructure)
ll_thoai_220601: Voice traffic customers usage
nod_psll_thoai_220601: Number of days using voice calls
so_lan_nap_the_220601: Number of times to top up the card (top up the account for consumption)
so_lan_nap_topup_220601: TOP up is a modern form of top-up via banks or digital tools, customers with no value ie top up in the traditional way.
so_ngay_su_dung_220601: Number of days using one of their services: Voice, Data, SMS.
thiet_bi_220601: Device customers are using: 2G devices, 3G devices, 4G devices (Only customers with 4G devices can convert customers to 4G)
thuc_4g_220601: This field is the field that needs to be used to check whether the customer is actually 4G or not ==> I need to forecast that the group of customers with a value of 0 has the potential to convert to 1 in the next month.
tong_cuoc_goc_data_4_huong_22060: Spending of customers for Data services (VND)
tong_cuoc_goc_fn_220601: Customer's spending for all services provided on customer's phone number (Voice, SMS, Data, Vas) (VND)
tong_cuoc_goc_thoai_220601: Spending of customers on voice services (VND)
tong_ll_gprs_220601: Customer's data usage behavior (Unit GB) - like the type of customer's unit of measure when watching youtube/going to facebook.
tong_tien_nap_the_220601: Amount of money deposited into the account by the customer to spend
tong_tien_nap_topup_220601: Amount deposited into account by modern methods (Bank, digital payment)
tuoi_khach_hang_cut_level_220601: Age cycle (months)
user_id: subscriber ID (This is the encoding of the phone number)

**Methods**

After EDA the data to clean the data as well as find out the factors to include in the model, we decided to try the categorical models (labelled) to find out which model has the highest accuracy.

**Conclusions**
From the balance accuracy:
- Logistic Regression: 89% KNN: 90% Decision Tree: 99% Random Forest: 99%

Compared between Decision Tree and Random Forest, the F1 score of test set in Random Forest is a little bit higher --> We will choose Random Forest
