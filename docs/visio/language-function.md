---
title: Función LANGUAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite realizar operaciones de comparación entre distintas representaciones del idioma. Se recomienda usar para convertir los valores de las etiquetas de idioma de Internet Engineering Task Force (BCP 47) a valores de identificador de configuración regional (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327821"
---
# <a name="language-function"></a>Función LANGUAGE

Permite realizar operaciones de comparación entre distintas representaciones del idioma. Se recomienda usar para convertir los valores de las etiquetas de idioma de Internet Engineering Task Force (BCP 47) a valores de identificador de configuración regional (LCID).
  
## <a name="version-information"></a>Información de versiones

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **Idioma** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obligatorio  <br/> |**String** <br/> |El valor LCID o BCP 47 para el idioma.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="example"></a>Ejemplo

 `LANGUAGE("en-us")`
  
Devuelve un valor de ' 1033 '.
  
 `LANGUAGE("es-es")`
  
Devuelve un valor de ' 3082 '.
  

