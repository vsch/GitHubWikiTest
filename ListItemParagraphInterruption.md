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

## Loose Item Handling

Tests how all tight items are generated

- item 1
- item 2 
- item 3 
- item 4 

Test to see how trailing blank after item determines looseness

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

Test looseness with child items

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

Test to see which list items can interrupt another numbered list item's paragraphs

1. Bullet item can interrupt paragraph of a numbered list item
* item

<!--List Break-->

1. Empty bullet item with space can interrupt paragraph of a numbered list item
* 

<!--List Break-->

1. Empty bullet item without space can interrupt paragraph of a numbered list item
*

<!--List Break-->

1. Numbered one item can interrupt paragraph of a numbered list item
1. one item

<!--List Break-->

1. Empty Numbered one item with space can interrupt paragraph of a numbered list item 
1. 

<!--List Break-->

1. Empty Numbered one item without space can interrupt paragraph of a numbered list item 
1.

<!--List Break-->

1. Numbered non-one item can interrupt paragraph of a numbered list item
2. non-one item

<!--List Break-->

1. Empty Numbered non-one item with space can interrupt paragraph of a numbered list item
2. 

<!--List Break-->

1. Empty Numbered non-one item without space can interrupt paragraph of a numbered list item
2.

## List Item Indent Handling

Test how list indentation is determined

* item 1
 * item 2
  * item 3
   * item 4
    * item 5
     * item 6
      * item 7
       * item 8
        * item 9
         * item 10

Test if list indentation is determined on marker indent or content indent. If this and above
test differ in list structure, then content indent is used. Otherwise, marker indent.

*  item 1
 *  item 2
  *  item 3
   *  item 4
    *  item 5
     *  item 6
      *  item 7
       *  item 8
        *  item 9
         *  item 10

Test to see if having a blank line in list item makes a difference on indent column calcualtion.
If this list structure is the same as the one without blank lines, then had blank line status
does not affect indentation level.

* item 1

 * item 2
 
  * item 3
  
   * item 4
   
    * item 5
    
     * item 6
     
      * item 7
      
       * item 8
       
        * item 9
        
         * item 10

Test to see if first item indent affect list indentation processing, if structure differs from
same list but without leading first item space then yes.

 * item 1
  * item 2
   * item 3
    * item 4
     * item 5
      * item 6
       * item 7
        * item 8
         * item 9
          * item 10

Test where lazy continuation affects list item processing.

* item 1
       * item 2
* item 3
        * item 4

Test if it is `first first list` indent processing, or first direct parent list processing that
affects sub-list indentation. 

* item 1
 * item 2
  * item 4
    > * item 3
    >  * item 4
    >   * item 5

<!-- list break -->

* item 1
 * item 2
  * item 4
     > * item 3
     >  * item 4
     >   * item 5

Test shows where the boundary switch to indented code occurs. First paragraph is a paragraph,
the second is indented code.

-   test
    - sub item

         sub item child para

          indented code
          
---

1.  test
    1. sub item

          sub item child para

           indented code

<!-- list break -->

-   test

       item child para

        indented code
          
-   test
    - sub item

           sub item child para

            sub item indented code
          
---

1.  test

       item child para

        item indented code

1.  test
    1. sub item

           sub item child para

            sub item indented code

More extensive test to show where the boundary switch to indented code occurs. Sub-items first
paragraph is a paragraph, the second is indented code

* item 1
    
  item para 1
  
   item para 2
   
    item para 3
    
     item para 4
     
      item para 5
      
       item para 6
       
        item para 7
        
 * item 2
    
   item para 1
   
    item para 2
    
     item para 3
     
      item para 4
      
       item para 5
       
        item para 6
        
         item para 7
        
  * item 3
    
    item para 1
    
     item para 2
     
      item para 3
      
       item para 4
       
        item para 5
        
         item para 6
         
          item para 7
        
   * item 4
    
     item para 1
     
      item para 2
      
       item para 3
       
        item para 4
        
         item para 5
         
          item para 6
          
           item para 7
        
    * item 5
    
      item para 1
  
       item para 2
   
        item para 3
    
         item para 4
     
          item para 5
      
           item para 6
       
            item para 7

Test for how items with indent > first list item's indent but < previous item's content indent
are handled. Mainly, if they are handled in a weird way of treating the item as a sub-item of
the previous list item. There was one that did it that way, GitHub comments if I can remember
right, but now they switched to commonmark list handling with mods. Guess it is now GFC--GitHub
Flavoured Commonmark.

*  item 1
   * item 2
  * item 3

Test how headings in list items are handled, leading space allowed or not

* item 1

  # Heading 1

   ## Heading 2

    ### Heading 3

     #### Heading 4

      ##### Heading 5

       ###### Heading 6

  * item 2

    # Heading 1
    
     ## Heading 2
    
      ### Heading 3
    
       #### Heading 3
    
        ##### Heading 5
      
         ###### Heading 6

