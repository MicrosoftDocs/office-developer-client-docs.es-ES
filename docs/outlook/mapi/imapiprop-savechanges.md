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
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316635"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hace permanentes todos los cambios realizados en un objeto desde la última operación de guardado. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla lo que ocurre con el objeto cuando se llama al método **IMAPIProp:: SaveChanges** . Se pueden establecer los siguientes indicadores: 
    
NON_EMS_XP_SAVE
  
> Indica que el mensaje no se ha entregado desde un servidor de Microsoft Exchange. Este indicador debe usarse en combinación con el método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) y la marca ITEMPROC_FORCE para indicar a un almacén de PST que el mensaje es apto para el procesamiento de reglas antes de que el almacén de archivos de carpetas personales (PST) notifique a cualquier cliente de escucha que ha recibido el mensaje. Este procesamiento de reglas solo se aplica a los mensajes nuevos que se crean con [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) en un servidor que no es un servidor de Exchange, en cuyo caso el servidor de Exchange ya habrá procesado las reglas del mensaje. 
    
FORCE_SAVE 
  
> Los cambios se deben escribir en el objeto, reemplazando los cambios anteriores que se han realizado en el objeto y se debe cerrar el objeto. Debe establecerse el permiso de lectura y escritura para que la operación se realice correctamente. La marca FORCE_SAVE se usa después de una llamada anterior a **SaveChanges** devolvió MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> Los cambios deben confirmarse y el objeto debe mantenerse abierto para lectura. No se realizarán cambios adicionales. 
    
KEEP_OPEN_READWRITE 
  
> Los cambios deben confirmarse y el objeto debe mantenerse abierto para permiso de lectura y escritura. Esta marca suele establecerse cuando el objeto se abrió por primera vez para permiso de lectura y escritura. Se permiten los cambios posteriores en el objeto. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **SaveChanges** vuelva correctamente, posiblemente antes de que los cambios se hayan confirmado por completo. 
    
SPAMFILTER_ONSAVE
  
> Habilita el filtrado de correo no deseado en un mensaje que se está guardando. El soporte de filtrado de spam solo está disponible si el tipo de dirección de correo electrónico del remitente es Protocolo simple de transferencia de correo (SMTP) y el mensaje se está guardando en un almacén de un archivo de carpetas personales (PST).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El compromiso de los cambios se realizó correctamente.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** no puede mantener el objeto abierto para el permiso de solo lectura si KEEP_OPEN_READONLY está establecido o permiso de lectura y escritura si se establece KEEP_OPEN_READWRITE. No se confirman los cambios. 
    
MAPI_E_OBJECT_CHANGED 
  
> El objeto ha cambiado desde que se abrió.
    
MAPI_E_OBJECT_DELETED 
  
> El objeto se ha eliminado desde que se abrió.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp:: SaveChanges** hace permanentes los cambios de propiedad para los objetos que admiten el modelo de transacciones de procesamiento, como mensajes, datos adjuntos, contenedores de libretas de direcciones y objetos de usuario de mensajería. Los objetos que no admiten transacciones, como carpetas, almacenes de mensajes y secciones de perfil, hacen que los cambios sean permanentes inmediatamente. No se requiere ninguna llamada a **SaveChanges** . 
  
Dado que los proveedores de servicios no tienen que generar un identificador de entrada para sus objetos hasta que se hayan guardado todas las propiedades **** , es posible que la propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)del objeto no esté disponible hasta que se haya realizado el método **SaveChanges** . se ha llamado a. Algunos proveedores esperan hasta que se establece la marca KEEP_OPEN_READONLY en la llamada **SaveChanges** . KEEP_OPEN_READONLY indica que los cambios que se van a guardar en la llamada actual serán los últimos cambios que se realizarán en el objeto. 
  
Algunas implementaciones del almacén de mensajes no muestran los mensajes recién creados en una carpeta hasta que un cliente guarda los cambios en el mensaje mediante **SaveChanges** y libera los objetos de mensaje mediante el método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Además, algunas implementaciones de objetos no pueden generar **** una propiedad de un objeto de recién creado hasta que se haya llamado a **SaveChanges** , y algunos solo pueden hacerlo después de llamar a **SaveChanges** mediante KEEP_OPEN_READONLY establecido en _ulFlags_.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si recibe la marca KEEP_OPEN_READONLY, tiene la opción de dejar el acceso del objeto como de lectura y escritura. Sin embargo, un proveedor nunca puede dejar un objeto en un estado de solo lectura cuando se pasa la marca KEEP_OPEN_READWRITE.
  
Cuando un cliente guarda varios datos adjuntos en varios mensajes, llama al método **SaveChanges** para todos los datos adjuntos y cada mensaje. Con frecuencia, los clientes establecerán MAPI_DEFERRED_ERRORS para cada una de estas llamadas, excepto la última. Puede devolver errores con la última llamada o con llamadas anteriores. Puede incluso omitir la marca. 
  
Si KEEP_OPEN_READWRITE o KEEP_OPEN_READONLY se configura junto con MAPI_DEFERRED_ERRORS, puede pasar por alto la solicitud de aplazamiento de error. Si MAPI_DEFERRED_ERRORS no se establece en _ulFlags_, se puede devolver uno de los errores aplazados anteriormente para la llamada a **SaveChanges** . 
  
El hecho de que un proveedor de transporte remoto proporcione una implementación funcional de este método es opcional y depende de otras opciones de diseño de la implementación. Si implementa este método, hágalo de acuerdo con la documentación aquí. Dado que los objetos Folder y status no se transaccionan, como mínimo, la implementación de **SaveChanges** de un proveedor de transporte remoto debe devolver S_OK sin realizar ningún trabajo realmente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si un cliente pasa KEEP_OPEN_READONLY, llama al método [IMAPIProp:: SetProps](imapiprop-setprops.md) y, a continuación, llama de nuevo a **SaveChanges** , se podría producir un error en la misma implementación. 
  
Después de recibir MAPI_E_NO_ACCESS de una llamada en la que estableció KEEP_OPEN_READWRITE, seguirá teniendo permiso de lectura y escritura en el objeto. Puede llamar a **SaveChanges** de nuevo, pasando la marca KEEP_OPEN_READONLY o sin marcadores con KEEP_OPEN_SUFFIX. 
  
El hecho de que un proveedor admita la marca KEEP_OPEN_READWRITE depende de la implementación del proveedor. 
  
Para indicar que la única llamada que debe realizarse en el objeto después de que **SaveChanges** es **IUnknown:: Release**, no establezca ningún marcador para el parámetro _ulFlags_ . Un error de **SaveChanges** indica que no pudo hacer permanentes los cambios pendientes. Los diferentes proveedores administran la ausencia de indicadores en la llamada de **SaveChanges** de forma diferente. Algunos proveedores tratan este estado de la misma forma que KEEP_OPEN_READONLY; otros proveedores la interpretan del mismo modo que KEEP_OPEN_READWRITE. Sin embargo, otros proveedores apagan el objeto cuando no reciben marcas en la llamada de **SaveChanges** . 
  
Algunas propiedades, normalmente las propiedades calculadas, no se pueden procesar hasta que se llame a **SaveChanges** y, en algunos casos, se **libere**.
  
Al realizar cambios masivos, como guardar datos adjuntos en varios mensajes, diferir el procesamiento de errores estableciendo la marca MAPI_DEFERRED_ERRORS en _ulFlags_. Si guarda varios datos adjuntos en varios mensajes, realice una llamada de **SaveChanges** a cada adjunto y una llamada de **SaveChanges** a cada mensaje. Establezca la marca MAPI_DEFERRED_ERRORS para cada llamada de datos adjuntos y para todos los mensajes excepto para la última. 
  
Si **SaveChanges** devuelve MAPI_E_OBJECT_CHANGED, compruebe si se ha modificado el objeto original. Si es así, avise al usuario, que puede solicitar que los cambios sobrescriban los cambios anteriores o guardar el objeto en otra ubicación. Si se ha eliminado el objeto original, avise al usuario para que le dé la oportunidad de guardar el objeto en otra ubicación. 
  
No puede llamar a **SaveChanges** con la marca FORCE_SAVE en un objeto abierto que se ha eliminado. 
  
Si **SaveChanges** devuelve un error, el objeto cuyos cambios se guardarán permanecerá abierto, independientemente de los marcadores establecidos en el parámetro _ulFlags_ . 
  
> [!IMPORTANT]
> El _ulFlags_ NON_EMS_XP_SAVE y SPAMFILTER_ONSAVE podrían no estar definidos en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con los siguientes valores: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Para obtener más información, consulte [Guardar propiedades MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Vea también



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Guardar propiedades MAPI](saving-mapi-properties.md)

