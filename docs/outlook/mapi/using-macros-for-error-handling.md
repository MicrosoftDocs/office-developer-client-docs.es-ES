---
title: Uso de macros para el control de errores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435568"
---
# <a name="using-macros-for-error-handling"></a>Uso de macros para el control de errores

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay varias macros que facilitan el trabajo con valores HRESULT.
  
Hay dos conjuntos de macros que comprueban si hay errores o correctos: HR_SUCCEEDED y HR_FAILED, y SUCCEEDED y FAILed. SUCCEEDED es el mismo que HR_SUCCEEDED y FAILed es el mismo que HR_FAILED.
  
En este caso, use la macro **ResultFromScode** para establecer la variable HRESULT en el valor HRESULT correspondiente para S_OK. 
  
En la tabla siguiente se describen brevemente las macros usadas con frecuencia.
  
|**Macro**|**Descripción**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Construye un HRESULT a partir de sus componentes.  <br/> |
|**HR_SUCCEEDED** <br/> |Prueba un valor HRESULT para una condición de éxito o advertencia.  <br/> |
|**HR_FAILED** <br/> |Prueba un HRESULT para una condición de error.  <br/> |
|**HRESULT_CODE** <br/> |Extrae la parte del código de error de HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrae la utilidad de HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrae el bit de gravedad de la gravedad.  <br/> |
|**REALIZA** <br/> |Prueba un valor HRESULT para una condición de éxito o advertencia.  <br/> |
|**ERRÓNEA** <br/> |Prueba un HRESULT para una condición de error.  <br/> |
   

