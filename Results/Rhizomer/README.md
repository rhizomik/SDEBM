# SDEBM Results for Rhizomer

This document reports the results for the SDEBM benchmark for the [Rhizomer](http://rhizomik.net/rhizomer/) tool, a semantic data exploration and visualization tool. Rhizomer automatically generates, after analyzing the semantic dataset, some user interface components to explore it. First, they facilitate gaining an overview of the dataset structure, concretely menus, TreeMaps, site maps and site indexes. Then, zooming and filtering into details through facets and the ability to pivot among sets of interrelated resources.

## Summary

Two [Quality in Use metrics](http://www.jucs.org/jucs_19_8/using_SWET_QUM_to) have been used, one about effectiveness and the other about efficiency:

* **Task Success** (effectiveness): what proportion of one task is completed. 0% if not possible to complete or 100% otherwise.
* **Interaction Steps** (efficiency): how many clicks C and how many typing events T are required at least to complete the task.

|Benchmark|Task Success|Interaction Steps|
|---------|-------------|----------------|
|1a       |0%           |-               |
|1b       |100%         |5C/1T           |
|2        |             | |
|3        |             | |
|4        |             | |
|5        |             | |

## Results per Benchmarks

**Task 1a**. [Find products for a given set of features combined](Benchmarks/1a.md)

This task cannot be performed because Rhizomer does not provide a way to define that all the selected values of a facet, in this case the productFeature facet, should be present at the same time for a given resource.

**Task 1b**. [Find products for a given set of alternative features](Benchmarks/1b.md)

Interaction steps:

1. Over Top Menu “ProductType”.
1. Click “Sheeny” from submenu.
1. Click “Show values” for facet “Product Feature”.
1. Check facet value “stroboscopes”.
1. Type in the “Search Product Feature” input box “gadget...”.
1. Click “gadgeteers” from the input box autocomplete recommendations.
1. Set the left side of the slider for facet “Product Property Numeric1” to “450”. (Or type “450” in the “From” input box for facet “Product Property Numeric1” and then press tabulator).

**Task 2**. [Retrieve basic information about a specific product for display purposes](Benchmarks/2.md)

From Query 1b Rhizomer shows the list of selected products and a short description for each one (label, types and comment). Click any product to retrieve all the metadata for the selected product..

Interaction steps:

1. Click product label “boozed”.

**Task 3**. [Find products having some specific features and not having one feature](Benchmarks/3.md)

This task is not currently possible using Rhizomer because it does not provide a way to negate facet values.

When this feature is implemented, these will be the interaction steps:

1. Over Top Menu “ProductType” and click “Sheeny” from submenu.
1. Click “Show values” for facet “Product Feature”.
1. Check facet value “stroboscopes”.
1. Type in the “Seach Product Feature” input box “gadget”.
1. Click “gadgeteers” from the input box autocomplete recommendations.
1. **TODO** Mark that the “gadgeteers” value should NOT be present
1. Set the left side of the slider for facet “Product Property Numeric1” to “300”.
1. Set the right side of the slider for facet “Product Property Numeric3” to “400”.

**Task 4**. [Find products matching two different sets of features](Benchmarks/4.md)

It cannot be performed using Rhizomer because it currently does not support AND for facet value neither the union of different query patterns.

**Task 5**. [Find products that are similar to a given product](Benchmarks/5.md)

The user can look for a specific product. As a result, the corresponding faceted view for it is generated and a query where the restriction is that the product is the one selected. The faceted view can be then used to select all the product features of the selected product. The user can also see the values for the numeric properties and manually set the ranges in the corresponding facet sliders. Finally, the user can remove the restriction for the specific product while keeping the rest of restrictions to retrieve similar products.

**Task 6**. [Find products having a name that contains some text](Benchmarks/6.md)

The user can directly use the “Quick search...” input box at the top, type “water” and a list of entities whose label contains “water” is shown, from where the user can select the one he is interested in.

Alternative: click “Product” in the menu and then use the “label” facet to search for label values containing water.

Alternative: not supported yet, “Quick search...” in addition to autocomplete user input also performs free text search and shows results in a view faceted by entity type.

**Task 7**. [Retrieve in-depth information about a specific product including offers and reviews](Benchmarks/7.md)

Interaction steps:

1. The user types “waterski...” in the search field and selects the product “waterskiing sharpness horseshoes”.
1. Click “See related Offers” at the bottom of the product description. Now showing faceted view for the product offers.
1. Click “Vendor” in right column “Related to...”. (Or in the “Vendor” facet click “Filter Vendor”). The faceted view for product offer vendors is shown.
1. Click “Show values” for the “Country” facet.
1. Check “CN” for China. Details for the two chinese vendors having offers for the product are shown.
1. Click “Offer” in the breadcrumbs (or “Offer” in right column “Back to...” or “Filter Offer” in the “Is Vendor of Offer” facet). Details for the five offers by Chinese vendors are shown.
1. Click “Show values” for the “Valid to” facet. There is no range selector for date facets, the user has to check each relevant date manually.
1. Check “2008-06-13”, the first date after “2008-05-28”.
1. Check “2008-07-10”, the second one.
1. Check “2008-08-04”, the last one. The details for the 3 selected offers are shown.
1. Click “Product” in right column “Related to...”. (Or “Filter Product” in the “Product” facet). The details for the selected product and its faceted view are shown.
1. Click “Review” in right column “Related to...”. (Or “Filter Review” in the “Is Review For of Review” facet). Details for five reviews for the selected product are shown, including rating1, rating2 or both when available.

**Task 8**. [Give me recent reviews in English for a specific product](Benchmarks/8.md)

**Task 9**. [Get information about a reviewer](Benchmarks/9.md)

**Task 10**. [Get offers for a given product which fulfill specific requirements](Benchmarks/10.md)

**Task 11**. [Get all information about an offer](Benchmarks/11.md)

**Task 12**. [Export the chosen offer into another information system which uses a different schema](Benchmarks/12.md)