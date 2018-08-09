---
title: Función FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Devuelve el valor entero del identificador único para una fuente, especificado por nombre.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822181"
---
# <a name="font-function"></a>Función FONT

Devuelve el valor entero del identificador único para una fuente, especificado por nombre.
  
> [!NOTE]
> En la mayoría de los casos, el identificador de la fuente es específico del sistema. Aunque la fuente permanece establecida una vez utilizado en un archivo, la función de **fuente** proporciona acceso coherente a una fuente en particular a través de sistemas y versiones de Visio. Se recomienda que utilice la función de la **fuente** para asignar a las fuentes en lugar de hacer referencia a los identificadores de fuente directamente. 
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **Fuente** ( _"font_name_string"_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Obligatorio  <br/> |**string** <br/> |Nombre de la fuente.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

Si la cadena proporcionada para *font_name_string* no coincide con una fuente conocida, esta función devuelve #VALUE! error. 
  
## <a name="example"></a>Ejemplo

 `FONT("Calibri")`
  
Devuelve el valor de entero (4) que representa el identificador exclusivo para la fuente "Calibri".
  

