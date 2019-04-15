

library(shiny)
library(rsconnect)


# Define UI for application that draws a histogram
ui <- fluidPage(
   
   # Application title
   titlePanel("A sleepy survey"),
   
   # Sidebar  
  sidebarPanel("Thanks for checking out our site!"),

 # Show a plot of the generated distribution
   mainPanel(" ",
             checkboxGroupInput("checkGroup", label = h3 ("What would you like to learn more about?"), 
                      choices = list("If I have a sleep disorder" = 1, "The treatment for sleep disturbances" = 2, 
                                     "What's going on with autism and sleep" = 3, "How other autistics deal with sleep problems" = 4,
                                     "How parents or family members deal with children's sleep problems" = 5),
                      selected = 1),
      hr(),
   fluidRow(column(3)),
   
   shinydashboard::box(title = "Where to find more information....",  
                       actionButton(inputId='ab1', label="Sleep problems and ASD symptoms", 
                                           icon = icon("th"), 
                                           onclick ="window.open('https://iancommunity.org/ssc/sleep-problems-linked-more-severe-autism-symptoms', '_blank')"),
                       actionButton(inputId='ab1', label="Treating  sleep  disorders", 
                                           icon = icon("th"), 
                                           onclick ="window.open('https://www.tuck.com/autism-spectrum-disorder-and-sleep/#treatment_options_for_asd_related_sleep_problems', '_blank')"),
                       actionButton(inputId='ab1', label="Statement from the American Academy of Pediatrics", 
                                    icon = icon("th"), 
                                    onclick ="window.open('https://www.aap.org/en-us/about-the-aap/aap-press-room/Pages/Children-with-Autism-Spectrum-Disorder-Experience-Poor-Sleep-Habits.aspx', '_blank')"),
                       actionButton(inputId='ab1', label="Strategies for improving sleep", 
                                    icon = icon("th"), 
                                    onclick ="window.open('https://www.autism.org.uk/about/health/sleep.aspx', '_blank')")
                       )
      )
      )
   


# Define server logic required to draw a histogram
server <- function(input, output) {
   
  # You can access the values of the widget (as a vector)
  # with input$checkGroup, e.g.
  output$value <- renderPrint({ input$checkGroup })
}

# Run the application 
shinyApp(ui = ui, server = server)

