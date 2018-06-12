---
title: IDIOMA (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite las operaciones de comparación entre las representaciones de idioma diferente. Mejor se utiliza para convertir los valores de etiquetas (BCP 47) de idioma de Internet Engineering Task Force en valores del identificador de (configuración regional LCID) de configuración regional.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822429"
---
# <a name="language-function"></a>IDIOMA (función)

Permite las operaciones de comparación entre las representaciones de idioma diferente. Mejor se utiliza para convertir los valores de etiquetas (BCP 47) de idioma de Internet Engineering Task Force en valores del identificador de (configuración regional LCID) de configuración regional.
  
## <a name="version-information"></a>Información de versión

Versión agregada: Visio 2013 
  
## <a name="syntax"></a>Sintaxis

 **Idioma** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obligatorio  <br/> |**String** <br/> |El valor LCID o BCP 47 para el idioma.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

Integer
  
## <a name="example"></a>Ejemplo

 `LANGUAGE("en-us")`
  
Devuelve un valor de '1033'.
  
 `LANGUAGE("es-es")`
  
Devuelve un valor de '3082'.
  

