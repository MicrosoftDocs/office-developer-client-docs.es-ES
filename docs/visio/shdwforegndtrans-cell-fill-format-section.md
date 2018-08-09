---
title: Celda ShdwForegndTrans (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Determina el nivel de transparencia del color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823202"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>Celda ShdwForegndTrans (sección Formato de relleno)

Determina el nivel de transparencia del color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|
          0 -100
  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Observaciones

Los valores se redondean al porcentaje medio más próximo. Un valor de 100% es completamente transparente. Aunque una sombra que tiene un relleno transparente completamente el mismo en la página de dibujo aparece como una sombra que no tiene relleno, interactúa con otros objetos en la página de la misma manera como si su transparencia fuera 0%.
  
También puede usar el control deslizante del cuadro de diálogo **Sombra** para establecer este valor (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Sombra** y, a continuación, en **Opciones de sombra**). Este valor controla el valor de las transparencias de sombra de primer y segundo plano. Para establecer estos valores de forma independiente, debe escribirlos en la ventana ShapeSheet.
  
Para obtener una referencia a la celda ShdwForegndTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShdwForegndTrans  <br/> |
   
Para obtener una referencia desde un programa a la celda ShdwForegndTrans por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowFill** <br/> |
|Índice de celda:  <br/> |**visFillShdwForegndTrans** <br/> |
   

