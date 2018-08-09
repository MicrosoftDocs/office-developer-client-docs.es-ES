---
title: Celda Style (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Muestra el formato de caracteres que se aplica a un intervalo de texto en el bloque de texto de la forma.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823323"
---
# <a name="style-cell-character-section"></a>Celda Style (sección Caracteres)

Muestra el formato de caracteres que se aplica a un intervalo de texto en el bloque de texto de la forma.
  
|**Estilo**|**Valor**|**Constante de automatización**|
|:-----|:-----|:-----|
| Negrita  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| Cursiva  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| Subrayado  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| Versalitas  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>Comentarios

La celda Style contiene la información de formato que se aplica a un subconjunto del texto de la forma si la sección de caracteres contiene varias filas. En caso contrario, contiene información de formato para todo el texto de la forma.
  
El valor representa un número binario en el que cada bit indica un estilo de carácter. Por ejemplo, un valor de 3 representa texto en formato de negrita y cursiva. Si el valor de estilo es 0, el texto es texto sin formato o sin formato. Puede probar para un formato determinado con bits booleano\* funciones. Vea la documentación de programación para obtener más información acerca de estas funciones.
  
Para obtener una referencia a la celda Style por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Char.Style [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Style por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionCharacter** <br/> |
| Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCharacterStyle** <br/> |
   
 *Ejemplo* 
  
Suponga que en la celda Color de la primera fila de la sección de caracteres se establece la fórmula siguiente:
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
Entonces, si el primer carácter del texto de la forma está en negrita, el texto cubierto por la primera fila de propiedades de Character será azul (4); en caso contrario será verde (3). En este ejemplo se supone que se utilizan los colores predeterminados.
  
En el siguiente ejemplo se establece la celda Style en un programa. La primera instrucción hace referencia a la celda Style por su nombre, y la segunda por su índice. Ambas instrucciones ponen en cursiva el texto cubierto por la segunda fila de la sección de caracteres de una forma.
  

