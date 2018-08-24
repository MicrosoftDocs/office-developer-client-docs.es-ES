---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c12750b7899403e62b9c1603615e9fd6caa95eca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569529"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Hace permanentes los cambios realizados a un objeto desde la última operación de guardar. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla lo que ocurre con el objeto cuando se llama al método **IMAPIProp::SaveChanges** . Se pueden establecer los siguientes indicadores: 
    
NON_EMS_XP_SAVE
  
> Indica que no se ha entregado el mensaje de un servidor de Microsoft Exchange. Este indicador se debe usar en combinación con el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) y la marca ITEMPROC_FORCE para indicar a un almacén de archivos PST que el mensaje tiene derecho para reglas de procesamiento antes de que el almacén de carpetas personales (PST) de archivo se lo comunica cualquiera cliente de escucha que ha llegado el mensaje. Esta reglas de procesamiento sólo se aplica a los nuevos mensajes que se crean con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un servidor de Exchange, en cuyo caso el servidor de Exchange ya habría procesado reglas en el mensaje. 
    
FORCE_SAVE 
  
> Los cambios se deben escribirse en el objeto, reemplazar los cambios anteriores que se han realizado en el objeto, y se debe cerrar el objeto. Permiso de lectura y escritura se debe establecer para que la operación se realice correctamente. El indicador FORCE_SAVE se utiliza después de una llamada anterior a **SaveChanges** devolvió MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> Se deberían confirmar los cambios y el objeto se debe mantener abierto para lectura. No se realizarán cambios adicionales. 
    
KEEP_OPEN_READWRITE 
  
> Se deberían confirmar los cambios y el objeto se debe mantener abierto para el permiso de lectura y escritura. Este indicador normalmente se establece cuando se abre por primera vez el objeto de permiso de lectura y escritura. Se permiten los cambios posteriores en el objeto. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **SaveChanges** devolver de correctamente, posiblemente antes de que los cambios se han guardado por completo. 
    
SPAMFILTER_ONSAVE
  
> Permite contra correo no deseado filtrado en un mensaje que se va a guardar. Soporte técnico de filtrado de correo no está disponible sólo si el tipo de dirección de correo electrónico del remitente es el protocolo Simple de transferencia de correo (SMTP) y el mensaje se guarda en un almacén para un archivo de carpetas personales (PST).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El compromiso de cambios fue correcto.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** no se puede mantener el objeto abierto para el permiso de sólo lectura si KEEP_OPEN_READONLY está establecido, o el permiso de lectura y escritura si se establece KEEP_OPEN_READWRITE. No hay cambios se confirman. 
    
MAPI_E_OBJECT_CHANGED 
  
> El objeto ha cambiado desde que se abrió.
    
MAPI_E_OBJECT_DELETED 
  
> El objeto se ha eliminado desde que se abrió.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp::SaveChanges** realiza los cambios de propiedad permanente para los objetos que admiten el modelo de transacción de procesamiento, como mensajes, datos adjuntos, contenedores de libretas de direcciones y los objetos de usuario de mensajería. Objetos que no admiten transacciones, como las carpetas, los almacenes de mensajes y las secciones de perfil, realice cambios permanentes inmediatamente. Ninguna llamada a **SaveChanges** es necesaria. 
  
Debido a que no es necesario generar un identificador de entrada para sus objetos hasta que se han guardado todas las propiedades de los proveedores de servicios, la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de un objeto no esté disponible hasta después de su método **SaveChanges** se ha llamado. Algunos proveedores de esperar hasta que se establezca el indicador KEEP_OPEN_READONLY en la llamada de **SaveChanges** . KEEP_OPEN_READONLY indica que los cambios se guarden en la llamada actual serán los últimos cambios que se realizarán en el objeto. 
  
Algunas implementaciones de almacén de mensajes no mostrar recién creado mensajes hacer en una carpeta hasta que un cliente guarda el mensaje cambia mediante el uso de **SaveChanges** y libera los objetos de mensaje con el método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . Además, algunas implementaciones de objeto no pueden generar una propiedad de **entrada del objeto** para un objeto recién creado hasta que después se ha llamado al **SaveChanges** y algunas pueden hacerlo sólo una vez que se ha llamado al **SaveChanges** mediante el uso de KEEP_OPEN_READONLY establecer en _ulFlags_.
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si recibe la marca KEEP_OPEN_READONLY, tendrá la opción de salir de access del objeto como de lectura y escritura. Sin embargo, un proveedor de nunca puede dejar un objeto en un estado de sólo lectura cuando se pasa el indicador KEEP_OPEN_READWRITE.
  
Cuando un cliente guarda los datos adjuntos de varios a varios mensajes, se llama al método **SaveChanges** para todos los datos adjuntos y todos los mensajes. A menudo los clientes establecerá MAPI_DEFERRED_ERRORS para cada una de estas llamadas excepto el último. Puede devolver los errores con la última llamada o llamadas anteriores. Incluso puede pasar por alto la marca. 
  
Si se establece KEEP_OPEN_READWRITE o KEEP_OPEN_READONLY junto con MAPI_DEFERRED_ERRORS, puede omitir la petición de aplazamiento de error. Si MAPI_DEFERRED_ERRORS no está establecido en _ulFlags_, uno de los errores anteriormente diferidos puede devolver para la llamada de **SaveChanges** . 
  
Si un proveedor de transporte remoto proporciona una implementación funcional de este método es opcional y depende de otras opciones de diseño en su implementación. Si implementa este método, hacerlo de acuerdo con la documentación de aquí. Debido a que no se negocian objetos folder y objetos de estado, como mínimo implementación del proveedor de transporte remoto de **SaveChanges** debe devolver S_OK sin realmente realizar cualquier trabajo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si un cliente pasa KEEP_OPEN_READONLY, llama al método [IMAPIProp::SetProps](imapiprop-setprops.md) y, a continuación, llama a **SaveChanges** de nuevo, puede producirse un error en la misma implementación. 
  
Después de recibir una llamada MAPI_E_NO_ACCESS en el que establecer KEEP_OPEN_READWRITE, continuará tienen permiso de lectura y escritura para el objeto. Puede llamar a **SaveChanges** nuevo, pasando el indicador KEEP_OPEN_READONLY o sin marcadores con KEEP_OPEN_SUFFIX. 
  
Si un proveedor admite la marca KEEP_OPEN_READWRITE depende de la implementación del proveedor. 
  
Para indicar que la llamada sólo deben realizar en el objeto después de **SaveChanges** es **IUnknown:: Release**, no establezca marcadores para el parámetro _ulFlags indicado_ . Un error de **SaveChanges** indica que podrían no realizar los cambios pendientes permanente. Distintos proveedores de tratar la ausencia de indicadores en la llamada **SaveChanges** de forma diferente. Algunos proveedores de tratan este estado igual que KEEP_OPEN_READONLY; otros proveedores de interpretan el mismo que KEEP_OPEN_READWRITE. Aún otros proveedores apague el objeto cuando no reciben marcas en la llamada de **SaveChanges** . 
  
Algunas propiedades, propiedades calculadas por lo general, no se puede procesar hasta que se llame **SaveChanges** y, en algunos casos, la **versión**.
  
Cuando se realizan cambios de forma masiva, como guardar los datos adjuntos a varios mensajes, aplazar error al procesar estableciendo el indicador MAPI_DEFERRED_ERRORS en _ulFlags_. Si guarda los datos adjuntos de varios a varios mensajes, realizar una **SaveChanges** llamar a cada dato adjunto y uno **SaveChanges** llamar a cada mensaje. Establecer la marca MAPI_DEFERRED_ERRORS para cada llamada de datos adjuntos y para todos los mensajes excepto el último. 
  
Si **SaveChanges** devuelve MAPI_E_OBJECT_CHANGED, compruebe si se ha modificado el objeto original. Si es así, avisar al usuario, que ya sea puede solicitar que los cambios de sobrescribirán los cambios anteriores o guardar el objeto en otra ubicación. Si se ha eliminado el objeto original, advertir al usuario que conceda la oportunidad de guardar el objeto en otra ubicación. 
  
No se puede llamar a **SaveChanges** con la marca FORCE_SAVE en un objeto abierto que se ha eliminado. 
  
Si **SaveChanges** devuelve un error, abra el objeto cuyos cambios tenían que guardarse permanece, independientemente de los indicadores establecidos en el parámetro _ulFlags indicado_ . 
  
> [!IMPORTANT]
> El _ulFlags_ NON_EMS_XP_SAVE y SPAMFILTER_ONSAVE no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con los siguientes valores: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Para obtener más información, vea [Guardar las propiedades de MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Vea también



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Guardar las propiedades MAPI](saving-mapi-properties.md)

