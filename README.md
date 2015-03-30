# Ипотечный калькулятор

Адаптивный, сделан с использованием [Bootstrap](http://getbootstrap.com/) и [jQuery UI Slider](https://jqueryui.com/slider/). Заданные по умолчанию селекторы и значения можно менять с помощью параметров. Так же в ближайшем обновлении добавится поддержка для touch устройств, так как jQuery UI Slider "из коробки" не позволяет это делать.

> [Пример](http://kirenkov.me/mortgage-calculator/)

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
  
    // Стоимость квартиры (руб.)
    flatPriceSlider          :     '.apartment_price-slider', // Слайдер
    flatPriceInput           :     '.apartment_price-input',  // Вывод значения
    flatPriceMin             :     1000000,  // От
    flatPriceMax             :     15000000, // До

    // Первоначальный взнос (руб.)
    firstPaymentSlider      :     '.first_payment-slider', // Слайдер
    firstPaymentInput       :     '.first_payment-input',  // Вывод значения
    firstPaymentMin         :     0,        // От
    firstPaymentMax         :     15000000, // До
    firstPaymentCurrent     :     0,        // Значение по умолчанию

    // Сумма кредита (руб.)
    credSumSlider           :     '.credit_sum-slider', // Слайдер
    credSumInput            :     '.credit_sum-input', // Вывод значения
    credSumCheckbox         :     '.credit_sum-checkbox',  // Переключатель (checkbox)
    credSumMin              :     1000000,  // От
    credSumMax              :     15000000, // До
    credSumCurrent          :     8000000,  // Значение по умолчанию

    // Срок кредита (мес.)
    credDurationSlider      :     '.credit_duration-slider',   // Слайдер
    credDurationInput       :     '.credit_duration-input',    // Вывод значения
    credDurationCheckbox    :     '.credit_duration-checkbox', // Переключатель (checkbox)
    credDurationMin         :     1,   // От
    credDurationMax         :     240, // До
    credDurationCurrent     :     60,  // Значение по умолчанию

    // Ставка (%)
    credRateSlider          :     '.credit_rate-slider', // Слайдер
    credRateInput           :     '.credit_rate-input',  // Вывод значения
    credRateMin             :     5,  // От
    credRateMax             :     30, // До
    credRateCurrent         :     12, // Значение по умолчанию

    // Ежемесячный платеж (руб.)
    monthPaymentSlider      :     '.monthly_payment-slider',   // Слайдер
    monthPaymentInput       :     '.monthly_payment-input',    // Вывод значения
    monthPaymentCheckbox    :     '.monthly_payment-checkbox', // Переключатель (checkbox)
    monthPaymentMin         :     5000,   // От
    monthPaymentMax         :     1000000 // До
  });
});
```
