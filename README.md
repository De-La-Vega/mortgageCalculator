# Ипотечный калькулятор

Адаптивный, сделан с использованием [Bootstrap](http://getbootstrap.com/) и [jQuery UI Slider](https://jqueryui.com/slider/). Заданные по умолчанию селекторы и значения можно менять с помощью параметров. Так же в ближайшем обновлении добавится поддержка для touch устройств, так как jQuery UI Slider "из коробки" не позволяет это делать.

Инициализация со стандартными параметрами делается простым вызовом функции на обёртку:
```javascript
$(function(){
	$(".calc_init").mortgageCalculator();
});
```
<br>
Ниже запуск с доступными к изменению параметрами:
```javascript
$(function(){
	$(".calc_init").mortgageCalculator({
      flatPriceSlider          :     '.apartment_price-slider',
      flatPriceInput           :     '.apartment_price-input',
      flatPriceMin             :     1000000,
      flatPriceMax             :     15000000,
  
      firstPaymentSlider      :     '.first_payment-slider',
      firstPaymentInput       :     '.first_payment-input',
      firstPaymentMin         :     0,
      firstPaymentMax         :     15000000,
      firstPaymentCurrent     :     0,
  
      credSumSlider           :     '.credit_sum-slider',
      credSumInput            :     '.credit_sum-input',
      credSumCheckbox         :     '.credit_sum-checkbox',
      credSumMin              :     1000000,
      credSumMax              :     15000000,
      credSumCurrent          :     8000000,
  
      credDurationSlider      :     '.credit_duration-slider',
      credDurationInput       :     '.credit_duration-input',
      credDurationCheckbox    :     '.credit_duration-checkbox',
      credDurationMin         :     1,
      credDurationMax         :     240,
      credDurationCurrent     :     60,
  
      credRateSlider          :     '.credit_rate-slider',
      credRateInput           :     '.credit_rate-input',
      credRateMin             :     5,
      credRateMax             :     30,
      credRateCurrent         :     12,
  
      monthPaymentSlider      :     '.monthly_payment-slider',
      monthPaymentInput       :     '.monthly_payment-input',
      monthPaymentCheckbox    :     '.monthly_payment-checkbox',
      monthPaymentMin         :     5000,
      monthPaymentMax         :     1000000
  });
});
```
