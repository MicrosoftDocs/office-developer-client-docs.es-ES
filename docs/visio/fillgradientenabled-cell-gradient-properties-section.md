---
title: Celda FillGradientEnabled (sección Propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Determina si el degradado de relleno está habilitado para esta forma.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322494"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>Celda FillGradientEnabled (sección Propiedades de degradado)

Determina si el degradado de relleno está habilitado para esta forma. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El relleno degradado se muestra en la forma.  <br/> |
|FALSE  <br/> |Los rellenos degradados no se muestran en la forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **FillGradientEnabled** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | FillGradientEnabled  <br/> |
   
Para obtener una referencia desde un programa a la celda **FillGradientEnabled** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGradientProperties** <br/> |
| Índice de celda:  <br/> |* * visFillGradientEnabled * * <br/> |
   

