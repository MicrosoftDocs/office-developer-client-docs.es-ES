---
title: Función FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Devuelve el valor entero del identificador único de una fuente, especificado por nombre.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422176"
---
# <a name="font-function"></a>Función FONT

Devuelve el valor entero del identificador único de una fuente, especificado por nombre.
  
> [!NOTE]
> En la mayoría de los casos, el identificador de fuente es específico del sistema. Aunque la fuente permanece establecida una vez que se usa en un archivo, la función **FONT** proporciona un acceso coherente a una fuente determinada en todos los sistemas y versiones de Visio. Se recomienda usar la función **FONT** para asignar fuentes en lugar de hacer referencia a identificadores de fuente directamente. 
  
## <a name="version-information"></a>Información de versiones

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **FONT**( _"font_name_string"_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Obligatorio  <br/> |**string** <br/> |Nombre de la fuente.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Si la cadena proporcionada para  *font_name_string*  no coincide con una fuente conocida, esta función devuelve un #VALUE! error. 
  
## <a name="example"></a>Ejemplo

 `FONT("Calibri")`
  
Devuelve el valor entero (4) que representa el identificador único de la fuente "Calibri".
  

