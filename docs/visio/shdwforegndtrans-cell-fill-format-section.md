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
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435043"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>Celda ShdwForegndTrans (Sección de formato de relleno)

Determina el nivel de transparencia del color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0 -100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores se redondean al medio porcentaje más próximo. El valor 100% hace que sea totalmente transparente. Aunque una sombra que tiene un relleno completamente transparente aparece de la misma forma en la página de dibujo que una sombra sin relleno, interactúa con otros objetos de la página de la misma manera que si su transparencia fuera del 0%.
  
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
   

