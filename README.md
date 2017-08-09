## Hackerman Syntax

The hackerman syntax theme for atom

![A screenshot of your theme](https://raw.githubusercontent.com/sean-codes/hackerman-syntax/master/example.png?v=5)

## Links

|         |                                                       |
|---------|-------------------------------------------------------|
| Atom.io | https://atom.io/themes/hackerman-syntax               |
| GitHub  | https://github.com/sean-codes/hackerman-syntax        |
| Issues  | https://github.com/sean-codes/hackerman-syntax/issues |

## If you would like to mess with the fancy fonts
      //-------------------------------------------------------------------------------//
      //--------------------------| Mixin and Variables |------------------------------//
      //-------------------------------------------------------------------------------//

      .MIXIN_Firacode {
         font-family: 'Fira Code';
         font-style: normal;
         text-rendering: optimizeLegibility;
         font-weight: 500;
      }

      .MIXIN_Flottflott {
         vertical-align: baseline;
         font-family: 'flottflott', cursive;
         height: inherit;
         font-size: 1.6em;
         font-weight:lighter;
         line-height: 1rem;
      }

      .MIXIN_Megrim {
          vertical-align: baseline;
          font-family: 'Megrim', cursive;
          height: inherit;
          font-size: 1.1em;
          font-weight: bolder;
          line-height: 1rem;
      }

      .MIXIN_FANCYFONT{
         .MIXIN_Flottflott
      }

      .MIXIN_ligature{
         -webkit-font-feature-settings: "liga" off, "calt" off;
      }

      //-------------------------------------------------------------------------------//
      //-------------------------------| Selectors |-----------------------------------//
      //-------------------------------------------------------------------------------//
      atom-text-editor {
         .MIXIN_Firacode();

         .syntax--string.syntax--quoted,
         .syntax--string.syntax--regexp {
            .MIXIN_ligature();
         }

         .syntax--source > .syntax--keyword.syntax--syntax--control.syntax--flow,
         .syntax--storage:not(.syntax--arrow), .syntax--type .syntax--function,
         .syntax--keyword.syntax--control,
         .syntax--keyword:not(.syntax--sql):not(.syntax--operator):not(.syntax--assignment):not(.syntax--relational):not(.syntax--logical),
         .syntax--attribute-name.syntax--pseudo-element{
            .MIXIN_FANCYFONT();

            .syntax--punctuation{
               .MIXIN_Firacode;
               font-size:initial;
            }
         }
      }

## Install The Fonts:

|            |                                                       |
|------------|-------------------------------------------------------|
|  FiraCode  | https://github.com/tonsky/FiraCode                    |
|   Megrim   | https://fonts.google.com/specimen/Megrim              |
| FlottFlott | http://www.dafont.com/flottflott.font                 |
|  MR.ROBOT  | https://fontmeme.com/fonts/mr-robot-font/             |
