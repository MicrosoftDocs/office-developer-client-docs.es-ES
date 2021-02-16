---
title: Celda FillGradientDir (Sección de propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina la dirección del degradado de relleno. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406720"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Celda FillGradientDir (Sección de propiedades de degradado)

Determina la dirección del degradado de relleno. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso. 
  
> [!NOTE]
> Un degradado lineal es el único degradado que toma un valor de ángulo adicional (determinado por **la celda FillGradientDir).** Todas las demás direcciones de degradado tienen enumeraciones preestablecidas. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Degradado lineal. La **celda FillGradientAngle** determina la dirección del degradado.  <br/> |
|1-7  <br/> |Degradados radiales. El degradado se extiende hacia afuera en un círculo desde un punto central.  <br/> |
|8-12  <br/> |Degradados rectangulares. El degradado se extiende como una línea direccional desde un origen con un fundido de forma rectangular.  <br/> |
|13   <br/> |Degradado de la ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **FillGradientDir** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | FillGradientDir  <br/> |
   
Para obtener una referencia desde un programa a la celda **FillGradientDir** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGradientProperties** <br/> |
| Índice de celda:  <br/> |**visFillGradientDir** <br/> |
   

