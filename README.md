# DecisionTree
Clustering with Decision Tree and SVM on a MNIST dataset based on python

دیتاست استفاده شده در این پروژه، دیتاست MNIST است که شامل ۷۰۰۰۰ تصویر سیاه و سفید
از ارقام ۰ تا ۹ است که به صورت متوازن در ۱۰ کلاس مختلف توزیع شده اند، به طوری که هر کلاس
نماینده ی یکی از ارقام است. هر تصویر دارای ابعاد ۲۸ در ۲۸ پیکسل است و هر پیکسل مقداری بین
۰ تا ۲۵۵ دارد که شدت رنگ آن را نشان می دهد.

فاز اول Image Filtering است. در این فاز فرآیند Convolution یک کانال و فیلتر Sobel بر روی تصاویر دیتاست اعمال میشوند. پس از اعمال آنها، تابع آماده hog نیز بر روی تصاویر اعمال میشود.
فاز دوم Image Centering and PCA است. در این فاز ابتدا تصاویر centered خواهند شد سپس ابعاد آنها توسط PCA کاهش می یابد.
فاز سوم Desicion Tree Hyperparameter Tuning است. به جهت بهبود عملکرد درخت تصمیم از grid search و به جهت جلوگیری از overfitting از K-fold cross-validition استفاده شده است.
فاز چهارم به تحلیل دقت مدل میپردازد. از سه معیار Presicion, Recall و F1-Score استفاده شده است. همچنین نمایش نتایج با ایجاد confusion matrix و visualize کردن آن به صورت Heatmap انجام شده است.
در فاز پنجم هم از تکنیک pre-pruning به جهت جلوگیری از overfitting استفاده شده است.
