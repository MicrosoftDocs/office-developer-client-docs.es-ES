---
title: Celda FillGradientDir (sección de propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina la dirección del relleno degradado. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822130"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Celda FillGradientDir (sección de propiedades de degradado)

Determina la dirección del relleno degradado. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso. 
  
> [!NOTE]
> Un degradado lineal es el degradado sólo que toma un valor de ángulo adicionales (según lo determinado por la celda **FillGradientDir** ). Todas las demás direcciones de degradado tienen preestablecidas enumeraciones. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Degradado lineal. La celda **FillGradientAngle** determina la dirección del degradado.  <br/> |
|1-7  <br/> |Degradados radiales. El degradado se extiende hacia el exterior en un círculo desde un punto central.  <br/> |
|8-12  <br/> |Degradados rectangulares. El degradado se extiende como una línea direccional desde un origen con un desvanecimiento con forma rectangular.  <br/> |
|13  <br/> |Degradado de ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda **FillGradientDir** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | FillGradientDir  <br/> |
   
Para obtener una referencia a la celda **FillGradientDir** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGradientProperties** <br/> |
| Índice de celda:  <br/> |**visFillGradientDir** <br/> |
   

