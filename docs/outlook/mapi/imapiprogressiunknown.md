---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 42d09fd92edf4dc221b73dac4948e78a7c6898ac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589332"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Implementa un objeto de progreso que proporciona a las aplicaciones de cliente con un indicador de progreso. Un indicador de progreso es una presentación de la interfaz de usuario que muestra el porcentaje de finalización de una operación, como copiar carpetas entre almacenes de mensajes. Las aplicaciones MAPI y cliente implementan objetos de progreso y proveedores de servicios de usan. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de progreso  <br/> |
|Implementado por:  <br/> |MAPI y las aplicaciones cliente  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIProgress  <br/> |
|Tipo de puntero:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Actualiza el indicador de progreso con una visualización del progreso de la medida que se realiza hacia la finalización de la operación.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Devuelve marca configuración desde el objeto de progreso para el nivel de operación en la que se calcula la información de progreso.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Devuelve el número máximo de elementos en la operación de progreso que se muestra la información.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Devuelve el valor mínimo en el método [SetLimits](imapiprogress-setlimits.md) de progreso que se muestra la información.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Establece los límites superiores e inferiores para el número de elementos de la operación y los indicadores que controlan cómo se calcula la información de progreso de la operación.  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI incluye un parámetro _lpProgress_ en muchos de los métodos que realizan operaciones potencialmente prolongadas.  _lpProgress_ apunta a una implementación de cliente de un objeto de progreso. Los clientes que implementan la interfaz **IMAPIProgress** establezca este parámetro para que apunte a su implementación; los clientes que implementan **IMAPIProgress** establecer el parámetro en NULL. Para mostrar un indicador de progreso durante el procesamiento de la operación, proveedores de servicios de usar el objeto de progreso proporcionada por el cliente, si está disponible, o una implementación de MAPI (indicado cuando _lpProgress_ se establece en NULL). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivos**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiProgress.h y MapiProgress.cpp  <br/> |No disponible  <br/> |Si está habilitada la configuración de IMAPIProgress, MFCMAPI pasará una implementación de **IMAPIProgress** a todas las funciones que invoca MFCMAPI que aceptan una implementación.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

