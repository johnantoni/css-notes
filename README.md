css-notes
=========

### flexible fonts

    target / context = results
    
    24 / 16 = 1.5
    
    body { font-size:100%; } => 16px
    
    e.g.
    
    1. if base font size (100% set on body) equates to 16px (18px set by normalize.css)
    2. our target font size is 24px
    3. if we divide 24 / 16 we get 1.5
    
    so plug that 1.5 in as an em value and the new font size should be 24px
    
    h1 { font-size: 1.5em } => 24px
    


