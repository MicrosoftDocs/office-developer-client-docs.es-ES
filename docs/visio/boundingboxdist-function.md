---
title: BOUNDINGBOXDIST (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Devuelve la medida de la parte especificada del cuadro de límite de la forma.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821687"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST (función)

Devuelve la medida de la parte especificada del cuadro de límite de la forma. 
  
## <a name="version-information"></a>Información de versión

Versión agregada: Visio 2010 
  
## <a name="syntax"></a>Sintaxis

BOUNDINGBOXDIST (** *índice* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obligatorio  <br/> |**Número** <br/> |La parte de la forma cuadro de límite para medir y volver. Vea los comentarios para conocer los posibles valores.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Número**
  
## <a name="remarks"></a>Notas

 *Índice* puede ser uno de los valores siguientes. 
  
|**Item**|**Valor**|
|:-----|:-----|
|Ancho  <br/> |0  <br/> |
|Alto  <br/> |1  <br/> |
|Borde izquierdo a eje de la forma  <br/> |2  <br/> |
|Eje de la forma a borde derecho  <br/> |3  <br/> |
|Eje de la forma a borde superior  <br/> |4  <br/> |
|Borde inferior a eje de la forma  <br/> |5  <br/> |
|Centro del cuadro de límite a EjeX  <br/> |6  <br/> |
|Centro del cuadro de límite a EjeY  <br/> |7  <br/> |
   

