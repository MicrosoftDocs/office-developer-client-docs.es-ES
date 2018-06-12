---
title: Celda FillForegndTrans (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Determina el nivel de transparencia del color de primer plano de la trama de relleno de la forma.
ms.openlocfilehash: f9b09d67bc8d9ae851e86eaaa2ce1d36a92b2da2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822133"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a>Celda FillForegndTrans (Sección de formato de relleno)

Determina el nivel de transparencia del color de primer plano de la trama de relleno de la forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0 - 100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Observaciones

Los valores se redondean al porcentaje medio más próximo. El valor 100% hace que sea totalmente transparente. Aunque en la página de dibujo una forma con un relleno totalmente transparente y otra sin relleno aparecen igual, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del cero por ciento.
  
También puede establecer este valor mediante el control deslizante en el cuadro de diálogo **relleno** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **relleno**y, a continuación, haga clic en **Opciones de relleno**). Este valor controla el valor de transparencias de relleno de fondo y de primer plano. Para establecer estos valores de forma independiente, debe escribir en la ventana ShapeSheet.
  
Para obtener una referencia a la celda FillForegndTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |FillForegndTrans  <br/> |
   
Para obtener una referencia a la celda FillForegndTrans por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowFill** <br/> |
|Índice de celda:  <br/> |**visFillForegndTrans** <br/> |
   

