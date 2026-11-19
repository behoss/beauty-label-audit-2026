# Beauty label audit 2026: 1,641 cosmetic ingredient lists decoded

Source and full method: https://beautycomparison.com/research/label-audit

**Beauty label audit 2026** is a product-level dataset of 1,641 skincare, haircare, body, baby, sun, men's, nail and makeup products. Each product's full ingredient list (INCI) was checked by code against 12 ingredient families, so anyone can test what words such as "sensitive", "gentle", "natural" and "fragrance-free" on the front of a pack really mean.

## Headline findings

- 53% of products with "sensitive" in the name list parfum or fragrance (28 of 53).
- 56% of baby washes, lotions and creams contain added fragrance (30 of 54); 39% carry a labelled fragrance allergen.
- 64% of "gentle" or "mild" products contain added fragrance; 36% contain sulfates.
- 67% of "natural" or "organic" products carry a labelled fragrance allergen; 30% contain essential oils.
- Every product named "unscented" or "fragrance-free" (12 of 12) had no parfum, essential oils or labelled allergens.
- Only 15% of all products clear all 12 ingredient checks; in haircare, only 9% are free of fragrance and essential oils.
- Most common labelled allergens: linalool (26% of lists), limonene (24%), benzyl alcohol (16%).

## The file

`label-audit.csv`: 1,641 rows, one per product, 21 columns.

| Column | Meaning |
|---|---|
| `product_id` | Stable product id (also the page slug) |
| `brand`, `product` | Brand and product name |
| `category`, `type` | Category (skincare, haircare, makeup, body, mens, sun, nails, baby, fragrance) and product type |
| `ingredients` | Number of ingredients on the full list |
| `list_source` | Where the list came from: `brand` (the brand's own product page), `openbeautyfacts`, `retailer` or `regulator` |
| `list_retrieved` | Date the list was retrieved (5 to 10 November 2026) |
| `contains_fragrance` | 1 if the list has parfum, fragrance or aroma |
| `contains_essential_oils` | 1 if it has essential oils |
| `contains_eu_allergens` | 1 if it has a fragrance allergen that EU rules require on the label (linalool, limonene and others) |
| `contains_drying_alcohol` | 1 if it has drying alcohol (alcohol denat. and similar) |
| `contains_sulfates` | 1 if it has sulfate surfactants |
| `contains_silicones` | 1 if it has silicones |
| `contains_parabens` | 1 if it has parabens |
| `contains_mi_mci` | 1 if it has methylisothiazolinone or methylchloroisothiazolinone |
| `contains_formaldehyde_releasers` | 1 if it has formaldehyde-releasing preservatives |
| `contains_mineral_oil` | 1 if it has mineral oil or petrolatum |
| `contains_lanolin` | 1 if it has lanolin |
| `contains_chemical_uv_filters` | 1 if it has chemical UV filters |
| `page` | The product's page on beautycomparison.com, with the full decoded list |

## Method

Beauty Comparison took each product's full ingredient list from the brand's own product page or from Open Beauty Facts (two lists come from a retailer and a regulator), recorded the source and date, and checked every ingredient by code against the 12 families above. Claims were matched by keyword in the product name.

## Sources and licence

822 of the 1,641 ingredient lists come from [Open Beauty Facts](https://world.openbeautyfacts.org), made available under the Open Database License (ODbL); 817 come from the brands' own product pages, and one each from a regulator and a retailer listing. This dataset is published under the **Open Database License (ODbL) 1.0**: you may use, share and adapt it, with attribution and share-alike.

## How to cite

Beauty Comparison (Bez, editor). *Beauty label audit 2026: 1,641 cosmetic ingredient lists decoded*. 2026. https://beautycomparison.com/research/label-audit

DOI: [10.5281/zenodo.24356691](https://doi.org/10.5281/zenodo.24356691)

Also on [Zenodo](https://zenodo.org/records/24356691), [Hugging Face](https://huggingface.co/datasets/beautycomparison/beauty-label-audit-2026) and [Kaggle](https://www.kaggle.com/datasets/beautycomparison/beauty-label-audit-2026).

Author: Beauty Comparison (Bez, editor) · https://beautycomparison.com
