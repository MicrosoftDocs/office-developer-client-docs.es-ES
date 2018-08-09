---
title: Función de la izquierda (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Devuelve el carácter más a la izquierda o caracteres de una cadena de texto, en función del número de caracteres que especifique.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822440"
---
# <a name="left-function-visioshapesheet"></a>Función de la izquierda (VisioShapeSheet)

Devuelve el carácter más a la izquierda o caracteres de una cadena de texto, en función del número de caracteres que especifique.
  
## <a name="syntax"></a>Sintaxis

IZQUIERDA (** *texto* **, [, ** *número_caracteres_opcional* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |La cadena de texto que contiene los caracteres que se desean extraer.  <br/> |
| _número_caracteres_opcional_ <br/> |Opcional  <br/> |**Numeric** <br/> |Número de caracteres que se desean extraer.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Notas

El valor de _número_caracteres_opcional_ debe ser mayor o igual que cero (0). 
  
Si _número_caracteres_opcional_ es mayor que la longitud del texto, LEFT devuelve todo el texto. Si se omite _número_caracteres_opcional_ , se supone que es 1. 
  
## <a name="example"></a>Ejemplo

LEFT ("Enero 1, 2004", 3) 
  
Devuelve el valor "Ene". 
  

