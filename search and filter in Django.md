# search and filter in Django 

برای قرار دادن قسمت سرچ و مرتب سازی مراحل زیر را انجام میدهیم : 

1. اضافه کردن ```django_filters``` در نرم افزار های نصب شده در settings.py

2. ساختن فایل serializers.py و ساختن یک کلاس داخل آن که از ModelSerializer ارث بری کند 

   * ساخت کلاس داخلی meta و مشخص کردن model و  fields برای آن

3. ساخت کلاسی داخل views که از ListCreateAPIView ارث بری کند

   * مشخص کردن queryset و serializer_class

     * ```
       serializer_class = serializers.classname
       ```

4. اضافه کردن لیستی از search_fields ها به عنوان مواردی که در انها جستجو شود .
5. اضافه کردن لیستی از filterset_fields ها که در قسمت filter داخل سایت برای انها جایی برای جستجو ایجاد میشود .
6. اضافه کردن کد زیر که مشخص میکند چه مواردی در قسمت filter نمایش داده شود :

```filter_backends = [DjangoFilterBackend, SearchFilter, OrderingFilter]```

