# flexbox-demo

html file
1 container to hold flexbox items. Give class of flexbox-container. this will hold all our flexbox items
2 make div inside container with two classes one for flexbox-item, and another so we can style it individually
3 change to section demonstration

style file

1. .flexbox-container has no style so we will set display: flex;
   Flex is the value of css display property . Save and see all the items become same height and one row, shrink browswer and they scale to fit. This allow you to modify the parent container only and not have to adjust the style for its children! demo shrink browser, wide shows up on the left side of screen, this allows styling from the parent container without having to style the individual containers. So you can lay out your elements across rows and columns and align them inside the layout. YOu can specify how you want them to grow and shrink inside this parent container!
2. Main axis and cross axis. for column its flipped. so if you want to style elements on the main axis, use justify content property inside the parent container. flex start is default all elements align at start of main axis.
   flex-end, center, space-around, space-even
3. to align items on the cross axis use align items property. default is stretch which means items will stretch to fill the most amount of space vertically that they can... So we saw some of the smaller items grew to full size because of this default. If we want to keep their original size we use flex-start value on the align items property. center will center vertically.
   5 lets shrink and we will see that they get distorted. flex wrap: wrap will solve this. so we dont need media queries.
4. get rid of everything to display:flex
   flex-direction: column;
   justify-content: center;
   they dont center horizontally but theycenter inside the column vertically
   add height: 750px;
   now they center vertically bc justify content is using the main axis of column instead of row. Now align-items: center;


.flexbox-container {
    height: 800px;
    display: flex;
    flex-direction: column;
    justify-content:     center;
    align-items: center;
}

now the container is really for laying out spacing between items. and positioning items within container.
go back to just display: flex;
now by default when we shrink the container the items inside but if you want to prevent that to say the first item... uncomment 17. we can use flex-grow since we have all this extra space
