css-notes
=========

### flexible fonts

    TARGET div CONTEXT = RESULT
    
    24 / 16 = 1.5
    
    body { font-size:100%; } => 16px
    
    e.g.
    
    1. if base font size (100% set on body) equates to 16px (18px set by normalize.css)
    2. our target font size is 24px
    3. if we divide 24 by 16 we get 1.5
    
    so plug that 1.5 in as an em value and the new font size should be 24px
    
    h1 { font-size: 1.5em; } => 24px
    
#### link inside h1

    11 / 24 = 0.458333333333333
    
don't be tempted to round that down to 0.46, browsers are capable of handling this long number, just use it

    h1 a { 
      font-size: 0.458333333333333;
    }

#### write the calculations beside the css declarations

    h1 {
      font-size: 1.5em; /* 24px */
    }


    h1 a {
      font-size: 0.458333333333333; /* 11px */
    }

in the long run this will help you, also if need be create classname delcarations for typography elements.
    

    h1, .h1 {}
    h2, .h2 {}
    h3, .h3 {}
    h4, .h4 {}
    h5, .h5 {}
    h6, .h6 {}
    span, .span {}
    p, .p {}
    blockquote, .blockquote {}
    small, .small {}
    
### flexible grids

    #page { 
      margin: 36px auto;
      width: 960px;
    }
    .blog {
      margin: 0 auto 53px;
      width: 900px;
    }
    
...converted

    #page {
      margin: 36px auto;
      width: 90%;
    }
    .blog {
      margin: 0 auto 53px;
      width: 93.75% /* 900 div 960 = 0.9375 */
    }
      
...rather than em's we're using percentages as our context is different, obviously.

    
