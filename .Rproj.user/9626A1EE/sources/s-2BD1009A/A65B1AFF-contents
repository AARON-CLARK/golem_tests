#' counter UI Function
#'
#' @description A shiny Module.
#'
#' @param id,input,output,session Internal parameters for {shiny}.
#'
#' @noRd 
#'
#' @importFrom shiny NS tagList 
mod_counter_ui <- function(id){
  ns <- NS(id)
  tagList(
    actionButton(ns("button"), label = "Counter"),
    verbatimTextOutput(ns("out"))
  )
}
    
#' counter Server Function
#'
#' @noRd 
mod_counter_server <- function(input, output, session){
  ns <- session$ns
 
  count <- reactiveVal(0)
  
  observeEvent(input$button, {
    count(count() + 1)
  })
  
  output$out <- renderText({
    count()
  })
}
    
## To be copied in the UI
# mod_counter_ui("counter_ui_1")
    
## To be copied in the server
# callModule(mod_counter_server, "counter_ui_1")
 
