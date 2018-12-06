# Currency Converter

## Installation
Copy the folder `CurrencyConverter` into Statamic's addon folder.

## Usage
### Template
```
{{ currency_converter from="USD" to="EUR" amount="99.85" }}
    { converted }}
        <div class="bg-grey-darkest text-grey-lighest p-2 mx-4 shadow-inner">
            <span>≈ {{ currency }} {{ converted_amount }}</span>
        </div>
    {{ /converted }}
{{ /currency_converter }}`
```  

Also, using a variable you can pass a list of currencies to have multiple conversions. Just like that:
`{{ currency_converter from="USD" :to="currencies_list" amount="99.85" }}`

### API
Use `public function getConversionRate(string $from, string $to)` to get the conversion rate  
Use `public function convert(number $amount, string $from, string|array $to)` to get converted values
