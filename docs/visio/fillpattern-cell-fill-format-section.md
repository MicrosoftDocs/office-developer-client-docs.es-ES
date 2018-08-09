---
title: Celda FillPattern (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Determina la trama de relleno para la forma. Para especificar una trama de relleno personalizada, utilice la función USE en esta celda.
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822142"
---
# <a name="fillpattern-cell-fill-format-section"></a>Celda FillPattern (sección Formato de relleno)

Determina la trama de relleno para la forma. Para especificar una trama de relleno personalizada, utilice la función USE en esta celda.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Ninguno (relleno transparente).  <br/> |
|1  <br/> |Color de primer plano sólido.  <br/> |
|2 - 40  <br/> |Varias tramas de relleno que se corresponden con entradas de índice en el cuadro de diálogo **Relleno**.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor mediante el cuadro de diálogo **Relleno** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Relleno** y, a continuación, en **Opciones de relleno**).
  
Para obtener una referencia a la celda FillPattern por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |FillPattern  <br/> |
   
Para obtener una referencia desde un programa a la celda FillPattern por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowFill** <br/> |
|Índice de celda:  <br/> |**visFillPattern** <br/> |
   

