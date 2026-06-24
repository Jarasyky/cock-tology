# Phase 2 Checklist — First Cocktail Model

### Class hierarchy
- [ ] Create `CocktailRecipe` class
- [ ] Create `Ingredient` class with subclasses: `Spirit` → `Rum` → `WhiteRum`, `Mixer`, `Garnish`
- [ ] Create `MixingProcess` subclass

### Tier classes
- [ ] Create `T1Recipe`, `T2Recipe`, `T3Recipe` as global tier classes under `CocktailRecipe`
- [ ] Create `Mojito` class under `CocktailRecipe`
- [ ] Create `MojitoT1`, `MojitoT2`, `MojitoT3` under `Mojito`

### Object properties
- [ ] Create `hasSpirit` (domain: `CocktailRecipe`, range: `Spirit`)
- [ ] Create `hasMixer` (domain: `CocktailRecipe`, range: `Mixer`)
- [ ] Create `hasGarnish` (domain: `CocktailRecipe`, range: `Garnish`)

### Necessary conditions (what makes the reasoner work)
- [ ] `MojitoT1` — necessary condition: `hasSpirit some WhiteRum`
- [ ] `MojitoT2` — necessary condition: `hasSpirit some Rum`
- [ ] `MojitoT3` — necessary condition: `hasSpirit some Spirit`

### Individuals
- [ ] Create `HavanaClub3Year` individual, type `WhiteRum`
- [ ] Create `MojitoClassic` individual, type `Mojito`, add `hasSpirit HavanaClub3Year`

### Reasoner
- [ ] Select Pellet under **Reasoner** menu
- [ ] Run reasoner (**Reasoner → Start reasoner**)
- [ ] Verify `MojitoClassic` is inferred as `MojitoT1`, `MojitoT2`, `MojitoT3`

### Save & commit
- [ ] Save ontology to `ontology/cocktail.owl`
- [ ] Commit via lazygit
