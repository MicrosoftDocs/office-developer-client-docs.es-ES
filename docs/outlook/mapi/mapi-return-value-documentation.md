---
title: Documentación de valor deVuelto de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329718"
---
# <a name="mapi-return-value-documentation"></a>Documentación de valor deVuelto de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las entradas de referencia de este documento de referencia solo los valores devueltos que requieren algún control por parte de las aplicaciones cliente. Los valores deVueltos que indican condiciones de error comunes y pueden deducirse mediante la comprobación de errores no se incluyen en la documentación. Por ejemplo, muchos métodos de interfaz pueden devolver MAPI_E_INVALID_PARAMETER si el autor de la llamada especifica un valor incorrecto para un parámetro de entrada. Este valor no suele aparecer en el conjunto de valores devueltos esperados porque no es necesario buscar específicamente MAPI_E_INVALID_PARAMETER y no es necesario procesarlo de manera diferente a ningún otro error. Por otra parte, algunos proveedores de servicios no admiten la notificación de eventos y devolverán **** MAPI_E_NO_SUPPORT al método Advise realizado por los clientes a través de **IMAPISession**. Debido a que los clientes necesitan comprobar explícitamente este valor y proporcionar código para controlar la condición que representa en caso de que se produzca, MAPI_E_NO_SUPPORT se incluye en la lista de valores devueltos para [IMAPISession:: Advise](imapisession-advise.md).
  
La siguiente tabla describe los valores de error que se devuelven normalmente de los métodos y funciones, y requieren un control explícito de la parte de un cliente o proveedor de servicios. Estos valores se dividen en cuatro categorías: valores que indican datos de entrada no válidos, valores que indican problemas de recursos, valores que indican la incompatibilidad del juego de caracteres y valores que indican un error de origen desconocido.
  
|**Valor devuelto**|**Descripción**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Uno o varios de los parámetros pasados al método o funciones no son válidos.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Uno o más valores de un parámetro flags no eran válidos.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Hubo un problema al escribir o leer en el disco.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |No hay suficiente espacio en disco disponible para completar la operación.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |No hay suficiente memoria disponible para completar la operación.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |No hay suficientes recursos del sistema disponibles para completar la operación.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Existe una incompatibilidad en los juegos de caracteres admitidos por el autor de la llamada y la implementación.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Se ha producido un error de origen inesperado o desconocido.  <br/> |
   
Las constantes que representan valores devueltos de MAPI se enumeran en el MAPICODE. H archivo de encabezado. Algunas de las constantes se asignan a errores de Win32; la asignación de estas constantes a valores numéricos se puede encontrar en el archivo de encabezado Win32, WINERROR. H.
  
Los errores relacionados con los datos no válidos que pasa una persona que llama pueden determinarse a través de las funciones de la API de validación de parámetros proporcionadas por MAPI o un conjunto de macros. 
  
La incompatibilidad del juego de caracteres surge cuando se produce alguna de las siguientes situaciones:
  
- Un cliente o proveedor de servicios establece la marca MAPI_UNICODE en una llamada de método o función y la implementación no admite Unicode. Establecer MAPI_UNICODE indica que las cadenas de caracteres que se pasan como entrada son cadenas Unicode y que las cadenas de caracteres que se pasan como resultado se espera que sean cadenas Unicode.
    
- Un cliente o proveedor de servicios no establece la marca MAPI_UNICODE en un método o una llamada de función y la implementación solo admite Unicode.
    

