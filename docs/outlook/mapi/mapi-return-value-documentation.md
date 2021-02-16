---
title: Documentación del valor devuelto de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429694"
---
# <a name="mapi-return-value-documentation"></a>Documentación del valor devuelto de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las entradas de referencia de este documento de referencia solo devuelven los valores que requieren cierto control por parte de las aplicaciones cliente. Los valores devueltos que indican condiciones de error comunes y que se pueden deducir comprobando si hay errores no se incluyen en la documentación. Por ejemplo, muchos métodos de interfaz pueden devolver MAPI_E_INVALID_PARAMETER si un llamador especifica el valor incorrecto para un parámetro de entrada. Este valor normalmente no aparece en el conjunto de valores devueltos esperados porque no es necesario buscar específicamente MAPI_E_INVALID_PARAMETER y no es necesario procesarlo de forma diferente a cualquier otro error. Por otra parte, algunos proveedores de servicios no admiten la notificación de eventos y devolverán MAPI_E_NO_SUPPORT al método **Advise** realizado por los clientes a través de **IMAPISession**. Dado que los clientes necesitan comprobar explícitamente este valor y proporcionar código para controlar la condición que representa en caso de que se produzca, MAPI_E_NO_SUPPORT se incluye en la lista de valores devueltos para [IMAPISession::Advise](imapisession-advise.md).
  
En la tabla siguiente se describen los valores de error que normalmente se devuelven de métodos y funciones y que requieren un control explícito por parte de un cliente o proveedor de servicios. Estos valores se divide en cuatro categorías: valores que indican datos de entrada no válidos, valores que indican problemas de recursos, valores que indican incompatibilidad de juego de caracteres y valores que indican un error de origen desconocido.
  
|**Valor devuelto**|**Descripción**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Uno o varios de los parámetros pasados al método o funciones no eran válidos.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Uno o más valores para un parámetro flags no eran válidos.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Hubo un problema al escribir o leer en el disco.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |No había suficiente espacio en disco disponible para completar la operación.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |No había suficiente memoria disponible para completar la operación.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |No había suficientes recursos del sistema disponibles para completar la operación.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Existe una incompatibilidad en los conjuntos de caracteres admitidos por el autor de la llamada y la implementación.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Error de origen inesperado o desconocido.  <br/> |
   
Las constantes que representan valores devueltos de MAPI se enumeran en MAPICODE. Archivo de encabezado H. Algunas de las constantes se asignan a errores de Win32; La asignación de estas constantes a valores numéricos se puede encontrar en el archivo de encabezado Win32, WINERROR.H.
  
Los errores relativos a datos no válidos pasados por un llamador se pueden determinar a través de las funciones api de validación de parámetros proporcionadas por MAPI o un conjunto de macros. 
  
La incompatibilidad del juego de caracteres se produce cuando se produce alguna de las situaciones siguientes:
  
- Un cliente o proveedor de servicios establece MAPI_UNICODE marca en una llamada de método o función y la implementación no admite Unicode. Establecer MAPI_UNICODE indica que las cadenas de caracteres que se pasan como entrada son cadenas Unicode y que las cadenas de caracteres que se pasan hacia atrás como salida se espera que sean cadenas Unicode.
    
- Un cliente o proveedor de servicios no establece la marca MAPI_UNICODE en una llamada de método o función y la implementación solo admite Unicode.
    

