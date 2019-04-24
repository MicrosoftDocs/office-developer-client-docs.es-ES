---
title: BOUNDINGBOXDIST (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Devuelve la medida de la parte especificada del cuadro de límite de la forma.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348968"
---
# <a name="boundingboxdist-function"></a>Función BOUNDINGBOXDIST

Devuelve la medida de la parte especificada del cuadro de límite de la forma. 
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

BOUNDINGBOXDIST (* * *Índice* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obligatorio  <br/> |**Number** <br/> |Parte del cuadro de límite de la forma que se va a medir y devolver. Vea la sección Comentarios para los valores posibles.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Number**
  
## <a name="remarks"></a>Comentarios

 *Index* puede ser uno de los siguientes valores. 
  
|**Item**|**Value**|
|:-----|:-----|
|Width  <br/> |comprendi  <br/> |
|Height  <br/> |1  <br/> |
|Borde izquierdo a eje de la forma  <br/> |segundo  <br/> |
|Eje de la forma a borde derecho  <br/> |3  <br/> |
|Eje de la forma a borde superior  <br/> |4  <br/> |
|Borde inferior a eje de la forma  <br/> |2,5  <br/> |
|Centro del cuadro de límite a EjeX  <br/> |6,5  <br/> |
|Centro del cuadro de límite a EjeY  <br/> |0,7  <br/> |
   

