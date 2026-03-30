Step 1:

Replace the code in _product-card-gallery.liquid

Replace the following code in _product-card-gallery.liquid

{%- if product.available == false or product.compare_at_price > product.price and product.available -%}
    <div
      class="
        product-badges__badge product-badges__badge--rectangle
        {% if product.available == false %} color-{{ settings.badge_sold_out_color_scheme }}{% elsif product.compare_at_price > product.price %} color-{{ settings.badge_sale_color_scheme }}{% endif %}
      "
    >
      {%- if product.available == false -%}
        {{ 'content.product_badge_sold_out' | t }}
      {%- elsif product.compare_at_price > product.price -%}
        {{ 'content.product_badge_sale' | t }}
      {%- endif -%}
    </div>
  {%- endif -%}
With the following code

Copy Code
{%- assign current_variant = product.selected_or_first_available_variant -%}
{%- assign compare_at_price = product.compare_at_price_max -%}
{%- assign price = product.price -%}

{%- if product.available == false or compare_at_price > price -%}
    <div class="product-badges__badge product-badges__badge--rectangle
        {% if product.available == false %}
          color-{{ settings.badge_sold_out_color_scheme }}
        {% else %}
          color-{{ settings.badge_sale_color_scheme }}
        {% endif %}"
    >
      {%- if product.available == false -%}
        {{ 'content.product_badge_sold_out' | t }}
      {%- else -%}
        {%- assign max_discount = 0 -%}
        {%- for variant in product.variants -%}
          {%- if variant.compare_at_price > variant.price -%}
            {%- assign diff = variant.compare_at_price | minus: variant.price | times: 100 | divided_by: variant.compare_at_price -%}
            {%- if diff > max_discount -%}
              {%- assign max_discount = diff | round -%}
            {%- endif -%}
          {%- endif -%}
        {%- endfor -%}
        {%- if max_discount > 0 -%}{{ max_discount }}% OFF{%- endif -%}
      {%- endif -%}
    </div>
{%- endif -%}

Step 3:

Add block in Product Page Template

Goto Customize theme >> Product Page Template and Add New Block as per the screenshot below:

[!(https://websensepro.com/wp-content/uploads/2025/05/price-code-block.png)]

[![Show Sale Discount Percentage in Shopify](https://i.ytimg.com/vi/ynLP7Wqx-Vc/maxresdefault.jpg)](https://youtu.be/ynLP7Wqx-Vc?list=PLvT_6E7D1NZIlHa09cgswsjD9QunUpHKy)
