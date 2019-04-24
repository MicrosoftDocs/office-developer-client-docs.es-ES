---
title: IUnknown método imapiprogress
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
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270080"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Implementa un objeto Progress que proporciona a las aplicaciones cliente un indicador de progreso. Un indicador de progreso es una presentación de interfaz de usuario que muestra el porcentaje de finalización de una operación, como copiar carpetas entre almacenes de mensajes. Las aplicaciones cliente y MAPI implementan los objetos de progreso y los proveedores de servicios los usan. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Expuesto por:  <br/> |Objetos de progreso  <br/> |
|Implementado por:  <br/> |MAPI y aplicaciones cliente  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIProgress  <br/> |
|Tipo de puntero:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Actualiza el indicador de progreso con una presentación del progreso a medida que se realiza para completar la operación.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Devuelve la configuración de la marca del objeto Progress para el nivel de operación en el que se calcula la información del progreso.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Devuelve el número máximo de elementos en la operación para los que se muestra la información de progreso.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Devuelve el valor mínimo del método [SetLimits](imapiprogress-setlimits.md) para el que se muestra la información de progreso.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Establece los límites inferior y superior para el número de elementos de la operación y las marcas que controlan cómo se calcula la información de progreso de la operación.  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI incluye un parámetro _lpProgress_ en muchos de los métodos que llevan a cabo operaciones que pueden prolongarse.  _lpProgress_ apunta a una implementación de cliente de un objeto Progress. Los clientes que implementan la interfaz **método imapiprogress** establecen este parámetro para que apunten a su implementación; los clientes que no implementan **método imapiprogress** establecen el parámetro en NULL. Para mostrar un indicador de progreso durante el procesamiento de la operación, los proveedores de servicios usan el objeto Progress suministrado por el cliente, si está disponible, o una implementación MAPI (se indica cuando _lpProgress_ se establece en null). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Files**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MapiProgress. h y MapiProgress. cpp  <br/> |No aplicable  <br/> |Si la configuración método imapiprogress está habilitada, MFCMAPI pasará una implementación de **método imapiprogress** a todas las funciones que MFCMAPI invocan que aceptan una implementación.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

