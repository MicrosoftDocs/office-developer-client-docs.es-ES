---
title: LISTSHEETREF (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Devuelve una referencia de hoja a la forma del contenedor de lista que contiene la forma.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822504"
---
# <a name="listsheetref-function"></a>LISTSHEETREF (función)

Devuelve una referencia de hoja a la forma del contenedor de lista que contiene la forma.
  
## <a name="version-information"></a>Información de versión

Versión agregada: Visio 2010 
  
## <a name="syntax"></a>Sintaxis

LISTMEMBERCOUNT()
  
### <a name="return-value"></a>Valor devuelto

Referencia de ShapeSheet
  
## <a name="remarks"></a>Observaciones

Si la forma no es un miembro de la lista, la función LISTSHEETREF devuelve #REF!.
  
## <a name="example"></a>Ejemplo

LISTSHEETREF(1)!Height 
  
Devuelve el valor de la celda Height de la forma del contenedor de lista que contiene la forma. 
  

