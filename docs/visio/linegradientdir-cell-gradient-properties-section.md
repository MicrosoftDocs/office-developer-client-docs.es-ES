---
title: Celda LineGradientDir (sección Propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Determina la dirección del degradado de línea. Un degradado puede ser lineal, radial, rectangular o seguir una trayectoria.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350963"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>Celda LineGradientDir (sección Propiedades de degradado)

Determina la dirección del degradado de línea. Un degradado puede ser lineal, radial, rectangular o seguir una trayectoria. 
  
> [!NOTE]
> Un degradado lineal es el único degradado que toma un valor de ángulo adicional (según se determina por la celda **LineGradientDir** ). Todas las demás direcciones de degradado tienen enumeraciones preestablecidas. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |Degradado lineal. La celda **LineGradientAngle** determina la dirección del degradado.  <br/> |
|1-7  <br/> |Degradados radiales. El degradado se extiende hacia afuera en un círculo desde un punto central.  <br/> |
|8-12  <br/> |Degradados rectangulares. El degradado se extiende como una línea direccional desde un origen con una atenuación de forma rectangular.  <br/> |
|apartado  <br/> |Degradado de ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LineGradientDir** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LineGradientDir  <br/> |
   
Para obtener una referencia desde un programa a la celda **LineGradientDir** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGradientProperties** <br/> |
| Índice de celda:  <br/> |**visLineGradientDir** <br/> |
   

