---
title: Documentación de valor devuelto de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f2b8f87987f93ec152d4986131a6b7990273c28d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818203"
---
# <a name="mapi-return-value-documentation"></a>Documentación de valor devuelto de MAPI

  
  
**Hace referencia a**: Outlook 
  
Las entradas de referencia en esta referencia de documentos únicamente los valores devueltos que requieren algunos tratamiento por las aplicaciones cliente. Los valores devueltos que indican las condiciones de error comunes y se pueden deducir mediante la comprobación de errores no se incluyen en la documentación. Por ejemplo, muchos de los métodos de interfaz pueden devolver MAPI_E_INVALID_PARAMETER si un autor de la llamada especifica un valor incorrecto para un parámetro de entrada. Este valor normalmente no se incluye en el conjunto de valores devueltos esperados porque no hay ninguna necesidad de buscar específicamente para MAPI_E_INVALID_PARAMETER y sin necesidad de proceso de forma diferente de cualquier otro error. Por otro lado, algunos proveedores de servicios no admiten la notificación de eventos y devuelven MAPI_E_NO_SUPPORT al método **Advise** realizado por los clientes a través de **IMAPISession**. Debido a que los clientes necesitan comprobar este valor explícitamente y proporcionar código para controlar la condición que representa debe se producen, MAPI_E_NO_SUPPORT se incluye en la lista de los valores devueltos para [IMAPISession::Advise](imapisession-advise.md).
  
En la siguiente tabla se describe los valores de error que normalmente se devuelven de métodos y funciones y requieren un control explícito por parte de un proveedor de cliente o servicio. Estos valores se dividen en cuatro categorías: valores que indican los datos de entrada no válidos, los valores que indican problemas de recursos, los valores que indican la incompatibilidad del conjunto de caracteres y valores que indican el error de un origen desconocido.
  
|**Valor devuelto**|**Descripción**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Uno o varios de los parámetros pasan en el método o funciones no eran válidas.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Uno o varios valores para un parámetro de indicadores no son válidos.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Hubo un problema al escribir o leer desde el disco.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |No hay suficiente espacio en disco estaba disponible para completar la operación.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |No había suficiente memoria disponible para completar la operación.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |No hay suficientes recursos del sistema estaban disponibles para completar la operación.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Existe una incompatibilidad en los conjuntos de caracteres compatibles con el autor de la llamada y la implementación.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Se produjo un error de origen desconocido o inesperado.  <br/> |
   
Las constantes que representan los valores devueltos de MAPI se enumeran en la MAPICODE. Archivo de encabezado H. Algunas de las constantes se asignan a errores de Win32; la asignación de estas constantes para los valores numéricos se puede encontrar en el archivo de encabezado de Win32, archivo WINERROR. H.
  
Errores relacionados con los datos no válidos que se pasó un autor de la llamada se pueden determinar a través de las parámetro validación API funciones proporcionadas por MAPI o un conjunto de macros. 
  
Incompatibilidad de conjunto de caracteres se produce cuando se produce uno de los siguientes casos:
  
- Un proveedor de servicio o cliente establece el indicador MAPI_UNICODE en una llamada de método o la función y la implementación no es compatible con Unicode. Configuración de MAPI_UNICODE indica que las cadenas de caracteres que se pasó como entrada son cadenas Unicode y que se pasan como resultado las cadenas de caracteres se prevé que las cadenas Unicode.
    
- Un proveedor de servicio o cliente no establece el indicador MAPI_UNICODE en una llamada de método o la función y la implementación sólo es compatible con Unicode.
    

