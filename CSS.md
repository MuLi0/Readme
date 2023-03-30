# 布局
## flex布局
.container{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    align-content: center;
}
.item{
    order: 1;
    flex-grow: 1;
    flex-shrink: 1;
    flex-basis: auto;
    flex: flex-grow,flex-shrink,flex-basic;
}

## grid布局
.container{
    display: grid;
    grid-template-columns: 1fr;
    align-items: center;
    justify-items: center;
    align-content: center;
    justify-content: center;
    gap: 24px;
    column-gap: 24px;
    row-gap: 24px;
    grid-template-areas: 
        "header header header"
        "sidebar content content"
        "footer footer footer";
}
header{
    grid-area: header;
}