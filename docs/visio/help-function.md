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
description: Abre un archivo de Ayuda HTML con la palabra clave de especificadas en el cuadro de búsqueda.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822276"
---
# <a name="help-function"></a>HELP (función)

Abre un archivo de Ayuda HTML con la *palabra clave* palabra especificadas en el cuadro de **búsqueda** . 
  
## <a name="syntax"></a>Sintaxis

Ayuda ("** *filename.chm!keyword* **") 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _FileName.chm!Keyword_ <br/> |Obligatorio  <br/> |**String** <br/> | El nombre del archivo de Ayuda y la palabra clave para buscar.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si no se especifica ninguna *palabra clave* , la función HELP abre la página de contenido del archivo de ayuda. 
  
## <a name="example"></a>Ejemplo

Help("Visio.chm!ShapeSheet") 
  
Abre el archivo de Ayuda de Visio y muestra una lista de temas cuyas palabra clave es "forma". 
  

