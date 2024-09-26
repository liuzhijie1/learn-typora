### tailwind

1. aspect-ration:  aspect-square aspect-auto aspect-video   设置元素的比例

2. Container mx-auto px-4      sm  640  md 768  lg 1024  xl 1280 2xl 1536

3. Columns-x  gap-8   hover:columns-3   md:columns-3

4. Box-deciration-clone box-decoration-slice

5. Box-border box-content

6. ```css 
   block inline-block inline flex inline-flex table inline-table table-caption
   table-cell table-column table-column-group table-footer-group table-header-group
   table-row-group table-row flow-root grid inline-grid contents list-item hidden
   ```

7. Float-start float-end float-right float-left float-none

8. Clear-start celar-end clear-left clear-right clear-both clear-none

9. Isolate  isolation-auto

10. ```css
    /* object-fit 属性的取值 */
    object-fit: fill; /* 默认值，内容会拉伸以填充整个容器，可能会失去比例 */
    object-fit: contain; /* 内容保持原始比例，同时确保内容完全在容器内，可能会有空白区域 */
    object-fit: cover; /* 内容保持原始比例，完全覆盖容器，可能会裁剪内容 */
    object-fit: none; /* 内容保持原始比例，不进行任何调整，可能会溢出容器 */
    object-fit: scale-down; /* 内容根据需要缩小以适应容器，但不放大 */
    
    object-contain  object-cover object-fill object-none  object-scale-down
    ```

11. ```css
    /* object-position 属性的取值 */
    object-bottom
    object-center
    object-left
    object-left-bottom
    object-left-top
    object-right
    object-right-bottom
    object-right-top
    object-top
    ```

12. ```css
    /* overflow  */
    overflow-auto
    overflow-hidden
    overflow-clip
    overflow-visible
    overflow-scroll
    overflow-x-auto
    overflow-y-auto
    overflow-x-hidden
    ```

13. ```css
    /*overscroll behavior   */
    overscroll-auto
    overscroll-contain
    overscroll-none
    overscroll-y-auto
    overscroll-y-contain
    overscroll-y-none
    overscroll-x-auto
    overscroll-x-contain
    overscroll-x-none
    ```

14. ```css
    /*  postion  */
    static
    fixed
    absolute
    relative
    sticky
    ```

15. ```css
    /* top right bottom left  */
    inset
    left-1
    right-1
    top-1
    bottom-1
    ```

16. ```css
    /* visibility */
    visible
    invisible
    collapse
    ```

17. ```css
    /* z-index */
    z-0
    z-10
    z-20
    z-30
    z-40
    ```

18. ```css
    /* flex. */
    flex                => display: flex
    basis-0             => flex-basis: 0px
    flex-row.           => flex-direction: row
    flex-row-reverse    => flex-direction: row-reverse
    flex-col            => flex-direction: column
    flex-col-reverse    => flex-direction: column-reverse
    flex-wrap.          => flex-wrap: wrap
    flex-wrap-reverse.  => flex-wrap: wrap-reverse
    flex-nowrap.        => flex-wrap: nowrap
    flex-1              => flex: 1 1 0%     -> flex-growth  flex-shrink  flex-basis
    flex-auto.          => flex: 1 1 auto
    flex-initial.       => flex: 0 1 auto
    flex-none           => flex: none
    grow     						=> flex-grow: 1
    grow-0              => flow-grow: 0
    shrink							=> flex-shrink: 1
    shrink 							=> flex-shrink: 0
    order-3							=> order: 3
    
    ```

19. ```css
    /* Grid template columns */
    grid								=> display: grid
    grid-cols-8 				=> grid-template-columns: repeat(8, minmax(0, 1fr))
    col-auto  					=> grid-column: auto;
    col-span-1					=> grid-column: span 1 / span 1;
    col-span-full 			=> grid-column: 1 / -1
    col-start-1					=> grid-column-start: 1   左闭右开
    col-start-auto			=> grid-column-start: auto
    col-end-1						=> grid-column-end: 1
    grid-row-1 					=> grid-template-rows: repeat(1, minmax(0, 1fr))
    grid-rows-none			=> grid-template-rows: none
    grid-rows-subgrid		=> grid-template-rows: subgrid
    row-auto 						=> grid-row: auto
    row-span-1					=> grid-row: span 1 / span 1
    row-span-full 			=> grid-row: 1 / -1
    row-start-1					=> grid-row-start: 1
    row-end-1						=> grid-row-end: 1
    row-end-auto				=> grid-row-end: auto
    grid-flow-row				=> grid-auto-flow: row
    grid-flow-col				=> grid-auto-flow: column
    grid-flow-dense			=> grid-auto-flow: dense
    grid-flow-row-dense => grid-auto-flow: row dense
    grid-flow-col-dense => grid-auto-flow: column dense
    auto-cols-auto			=> grid-auto-columns: auto
    auto-cols-min				=> grid-auto-columns: min-content
    auto-cols-max 			=> grid-auto-columns: max-content
    auto-cols-fr				=> grid-auto-columns: minmax(0, 1fr)
    auto-rows-auto			=> grid-auto-rows: auto
    auto-rows-min				=> grid-auto-rows: min-content;
    auto-rows-max 			=> grid-auto-rows: max-content
    auto-rows-fr				=> grid-auto-rows: minmax(0, 1fr)
    ```

20. Gap-4 

21. ```css
    /* Utilities for controlling how flex and grid items are positioned along a container's main axis. */
    justify-normal			=> justify-content: normal
    justify-start				=> justify-content: flex-start
    justify-end					=> justify-content: flex-end
    justify-center			=> justify-content: center
    justify-between     => justify-content: space-between
    justify-around			=> justify-content: space-around
    justify-evenly 			=> justify-content: space-evenly
    justify-stretch			=> justify-content: stretch
    ```

22. ```css
    /* Utilities for controlling how grid items are aligned along their inline axis. */
    justify-items-start   => justify-items: start
    justfiy-items-end			=> justify-items: end
    justify-items-center	=> justify-items: center
    justify-items-stretch	=> justify-items: stretch
    ```

23. ```css
    /* Utilities for controlling how an individual grid item is aligned along its inline axis. */
    justify-self-auto   		=> justify-self: auto
    justify-self-start			=> justify-self: start
    justify-self-end				=> justify-self: end
    justify-self-center			=> justify-self: center;
    justify-self-stretch		=> justify-self: stretch
    ```

24. ```css
    /* Utilities for controlling how rows are positioned in multi-row flex and grid containers. */
    content-normal 					=> align-content: normal
    content-center					=> align-content: center
    content-start						=> align-content: flex-start;
    content-end							=> align-content: flex-end
    content-between					=> align-content: space-between
    content-around					=> align-content: space-around
    content-evenly					=> align-content: space-evenly
    content-baseline				=> align-content: baseline
    content-stretch					=> align-content: stretch
    ```

25. ```css
    /* Utilities for controlling how flex and grid items are positioned along a container's cross axis. */
    items-start							=> align-items: flex-start;
    items-end								=> align-items: flex-end
    items-center						=> align-items: center
    items-baseline					=> align-items: baseline
    items-stretch						=> align-items: stretch
    ```

26. ```css
    /* Utilities for controlling how an individual flex or grid item is positioned along its container's cross axis. */
    self-auto							=> align-self: auto
    self-start						=> align-self: flex-start
    self-end							=> align-self: flex-end
    self-center						=> align-self: center
    self-stretch					=> align-self: stretch
    self-baseline					=> align-self: baseline
    ```

27. ```css
    /* Utilities for controlling how content is justified and aligned at the same time. */
    place-content-center  			=> place-content: center;
    place-content-start					=> : start
    place-content-end						=> : end
    place-content-between				=> : space-between
    place-content-around				=> : space-around
    place-content-evenly 				=> : space-evenly
    place-content-baseline			=> : baseline
    place-content-stretch				=> : stretch
    ```

28. ```css
    /* Utilities for controlling how items are justified and aligned at the same time. */
    place-items-start				=> place-items: start
    place-items-end					=> : end
    place-items-center			=> : center
    place-items-baseline		=> : baseline
    place-items-stretch			=> : stretch
    ```

29. ```css
    /* Utilities for controlling how an individual item is justified and aligned at the same time. */
    place-self-auto				=> place-self: auto
    place-self-start			=> : start
    place-self-end				=> : end
    place-self-center			=> : center
    place-self-stretch		=> : stretch
    ```

30. 

