# ------------------- Practicing Reprex ----------------------

# NOT A REPREX
library(tidyverse)
library(palmerpenguins)


penguins %>% 
  select(species, body_mass_g, flipper_length_mm, year) %>% 
  filter(species == "Chinstrap") %>% 
  str_to_lower(species) %>% 
  group_by(island) %>% 
  summarise(mean(body_mass_g, na.rm = TRUE),
            mean(flipper_length_mm, na.rm = TRUE))


### A REPREX

library(tidyverse)

warpbreaks %>% 
  mutate(wool = str_to_lower(wool))


penguins %>% 
  select(species, body_mass_g, flipper_length_mm, year, island) %>% 
  filter(species == "Chinstrap") %>% 
  mutate(str_to_lower(species)) %>% 
  group_by(island) %>% 
  summarise(mean(body_mass_g, na.rm = TRUE),
            mean(flipper_length_mm, na.rm = TRUE))

### A FIXED REPREX

dF <- tribble(
  ~dogs, ~age,
  "Buta", 2,
  "Teddy", 5,
  "Topa Topa", 5
)

library(tidyverse)

dF %>% 
  mutate(dogs = str_to_lower(dogs))

