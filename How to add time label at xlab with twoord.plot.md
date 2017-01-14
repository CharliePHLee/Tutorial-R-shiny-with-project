#How to add time label at xlab with twoord.plot
---
    title: "Present"
    author: "Miao Chien"
    date: "2016年8月25日"
    output: html_document
    ---
    ## 匯出精美的圖表
    ```{r diamonds, message=FALSE}
    install.packages("plotly")
    install.packages("ggplot2")
    library(plotly)
    library(ggplot2)

    set.seed(100)
    d <- diamonds[sample(nrow(diamonds), 1000), ]
    plot_ly(d, x = ~carat, y = ~price, color = ~carat,
        size = ~carat, text = ~paste("Clarity: ", clarity))

    ```
