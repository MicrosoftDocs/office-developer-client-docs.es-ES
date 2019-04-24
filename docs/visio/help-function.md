---
title: HELP (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Abre un archivo de ayuda HTML con la palabra clave especificada en el cuadro de búsqueda.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329977"
---
# <a name="help-function"></a>Función HELP

Abre un archivo de ayuda HTML con la *palabra clave* especificada en el cuadro de **búsqueda** . 
  
## <a name="syntax"></a>Sintaxis

AYUDA ("* * *filename. chm! keyword* * *") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _FILENAME. chm (palabra clave)_ <br/> |Obligatorio  <br/> |**String** <br/> | El nombre del archivo de Ayuda y la palabra clave para buscar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si no se especifica ninguna *palabra clave* , la función Help abre la página de contenido del archivo de ayuda. 
  
## <a name="example"></a>Ejemplo

AYUDA ("Visio. chm! ShapeSheet") 
  
Abre el archivo de Ayuda de Visio y muestra una lista de temas cuyas palabra clave es "forma". 
  

