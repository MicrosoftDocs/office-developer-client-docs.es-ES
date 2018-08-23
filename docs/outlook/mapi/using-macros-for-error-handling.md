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
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567128"
---
# <a name="using-macros-for-error-handling"></a>Uso de macros para el control de errores

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay varias macros para hacer que sea más fácil trabajar con los valores HRESULT.
  
Hay dos conjuntos de las macros que pruebas en busca de éxito o fracaso: HR_SUCCEEDED y HR_FAILED y SUCCEEDED y error. Se ha realizado correctamente es que el mismo que HR_SUCCEEDED y error es el mismo que HR_FAILED.
  
En este caso, use la macro **ResultFromScode** para establecer la variable HRESULT el valor HRESULT correspondiente para S_OK. 
  
Las macros usadas con más frecuencia se describen brevemente en la tabla siguiente.
  
|**Macro**|**Descripción**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Construye un HRESULT de sus componentes.  <br/> |
|**HR_SUCCEEDED** <br/> |Comprueba un HRESULT para un éxito o condición de advertencia.  <br/> |
|**HR_FAILED** <br/> |Pruebas de un HRESULT para una condición de error.  <br/> |
|**HRESULT_CODE** <br/> |Extrae la parte de código de error de HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrae las instalaciones de HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrae el bit de gravedad de la gravedad.  <br/> |
|**SE HA REALIZADO CORRECTAMENTE** <br/> |Comprueba un HRESULT para un éxito o condición de advertencia.  <br/> |
|**NO SE PUDO** <br/> |Pruebas de un HRESULT para una condición de error.  <br/> |
   

