## Bullet Mismatch Starts a New List

- item
+ item
* item

## Ordered List Item Sets List Start

2. Non One Start Item

## Mismatched List Item Type Handling

- Bullet List
1. With Ordered Item

<!-- list break -->

1. Ordered Item
- With Bullet List

## Item Looseness

- item 1
- item 2 
- item 3 
- item 4 

<!-- list break -->

- item 1

- item 2 
- item 3 
- item 4 

<!-- list break -->

- item 1
- item 2 

- item 3 
- item 4 

<!-- list break -->

- item 1
- item 2 

- item 3 
- item 4 

## List Item Looseness With Children

- item 1
    - item 1.1
- item 2 
    - item 2.1 
- item 3 
    - item 3.1 
- item 4 
    - item 4.1 

<!-- list break -->

- item 1

    - item 1.1
- item 2 
    - item 2.1 
- item 3 
    - item 3.1 
- item 4 
    - item 4.1 

<!-- list break -->

- item 1
    - item 1.1

- item 2 
    - item 2.1 
- item 3 
    - item 3.1 
- item 4 
    - item 4.1
    
!-- list break -->

- item 1
    - item 1.1
- item 2 

    - item 2.1 
- item 3 
    - item 3.1 
- item 4 
    - item 4.1 

<!-- list break -->

- item 1
    - item 1.1
- item 2 
    - item 2.1 
    
- item 3 
    - item 3.1 
- item 4 
    - item 4.1 

<!-- list break -->

- item 1
    - item 1.1
- item 2 
    - item 2.1 
- item 3 

    - item 3.1 
- item 4 
    - item 4.1 

<!-- list break -->

- item 1
    - item 1.1
- item 2 
    - item 2.1 
- item 3 
    - item 3.1 
    
- item 4 
    - item 4.1 

<!-- list break -->

- item 1
    - item 1.1
- item 2 
    - item 2.1 
- item 3 
    - item 3.1 
- item 4 

    - item 4.1 

<!-- list break -->

## List Items Interrupt Paragraphs

Bullet item can interrupt paragraph
* item

Empty bullet item with space can interrupt paragraph 
* 

Empty bullet item without space can interrupt paragraph
*

Numbered one item can interrupt paragraph
1. one item

Empty Numbered one item with space can interrupt paragraph
1. 

Empty Numbered one item without space can interrupt paragraph
1.

Numbered non-one item can interrupt paragraph
2. non-one item

Empty Numbered non-one item with space can interrupt paragraph
2. 

Empty Numbered non-one item without space can interrupt paragraph
2.


## List Items Interrupt Bullet Item Paragraphs

* Bullet item can interrupt paragraph of a bullet list item
* item

<!--List Break-->

* Empty bullet item with space can interrupt paragraph of a bullet list item
* 

<!--List Break-->

* Empty bullet item without space can interrupt paragraph of a bullet list item
*

<!--List Break-->

* Numbered one item can interrupt paragraph of a bullet list item
1. one item

<!--List Break-->

* Empty Numbered one item with space can interrupt paragraph of a bullet list item
1. 

<!--List Break-->

* Empty Numbered one item without space can interrupt paragraph of a bullet list item
1.

<!--List Break-->

* Numbered non-one item can interrupt paragraph of a bullet list item
2. non-one item

<!--List Break-->

* Empty Numbered non-one item with space can interrupt paragraph of a bullet list item
2. 

<!--List Break-->

* Empty Numbered non-one item without space can interrupt paragraph of a bullet list item
2.

## Bullet Mismatch Starts a New List

- item
+ item
* item
