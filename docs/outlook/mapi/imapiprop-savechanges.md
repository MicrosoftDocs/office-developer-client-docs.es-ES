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
  
Realiza de forma permanente los cambios realizados en un objeto desde la última operación de guardado. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Máscara de bits de marcas que controla lo que sucede con el objeto cuando se llama al método **IMAPIProp::SaveChanges.** Se pueden establecer las siguientes marcas: 
    
NON_EMS_XP_SAVE
  
> Indica que el mensaje no se ha entregado desde un Microsoft Exchange Server. Esta marca debe usarse en combinación con el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) y la marca ITEMPROC_FORCE para indicar a un almacén PST que el mensaje es apto para el procesamiento de reglas antes de que el almacén de archivos de carpetas personales (PST) notije a cualquier cliente de escucha que el mensaje ha llegado. Este procesamiento de reglas solo se aplica a los nuevos mensajes que se crean con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un Exchange Server, en cuyo caso el Exchange Server ya habría procesado reglas en el mensaje. 
    
FORCE_SAVE 
  
> Los cambios deben escribirse en el objeto, reemplazando los cambios anteriores realizados en el objeto y el objeto debe cerrarse. Se debe establecer el permiso de lectura y escritura para que la operación se pueda realizar correctamente. La FORCE_SAVE se usa después de que una llamada anterior a **SaveChanges** devolvía MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> Los cambios deben ser confirmados y el objeto debe mantenerse abierto para su lectura. No se realizarán cambios adicionales. 
    
KEEP_OPEN_READWRITE 
  
> Los cambios deben ser confirmados y el objeto debe mantenerse abierto para el permiso de lectura y escritura. Esta marca suele establecerse cuando el objeto se abrió por primera vez para el permiso de lectura y escritura. Se permiten los cambios posteriores en el objeto. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que SaveChanges** vuelva correctamente, posiblemente antes de que los cambios se hayan confirmado completamente. 
    
SPAMFILTER_ONSAVE
  
> Habilita el filtrado de correo no deseado en un mensaje que se está guardando. El soporte de filtrado de spam solo está disponible si el tipo de dirección de correo electrónico del remitente es Protocolo simple de transferencia de correo (SMTP) y el mensaje se está guardando en un almacén de un archivo de carpetas personales (PST).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El compromiso de los cambios se ha realizado correctamente.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** no puede mantener el objeto abierto para el permiso de solo lectura si KEEP_OPEN_READONLY está establecido, o permiso de lectura y escritura si KEEP_OPEN_READWRITE está establecido. No se confirma ningún cambio. 
    
MAPI_E_OBJECT_CHANGED 
  
> El objeto ha cambiado desde que se abrió.
    
MAPI_E_OBJECT_DELETED 
  
> El objeto se ha eliminado desde que se abrió.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIProp::SaveChanges** hace que los cambios de propiedad sea permanente para los objetos que admiten el modelo de transacciones de procesamiento, como mensajes, datos adjuntos, contenedores de libreta de direcciones y objetos de usuario de mensajería. Los objetos que no admiten transacciones, como carpetas, almacenes de mensajes y secciones de perfil, hacen cambios permanentes inmediatamente. No se requiere **ninguna llamada a SaveChanges.** 
  
Dado que los proveedores de servicios no tienen que generar un identificador de entrada para sus objetos hasta que se hayan guardado todas las propiedades, es posible que la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de un objeto no esté disponible hasta después de llamar a su **método SaveChanges.** Algunos proveedores esperan hasta que se KEEP_OPEN_READONLY marca en la **llamada SaveChanges.** KEEP_OPEN_READONLY indica que los cambios que se guardarán en la llamada actual serán los últimos cambios que se realizarán en el objeto. 
  
Algunas implementaciones de almacén de mensajes no muestran mensajes recién creados en una carpeta hasta que un cliente guarda los cambios de mensaje mediante **SaveChanges** y libera los objetos de mensaje mediante el método [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Además, algunas implementaciones de objetos no pueden generar una propiedad **PR_ENTRYID** para un objeto recién creado hasta después de llamar a **SaveChanges** y otras solo pueden hacerlo después de llamar a **SaveChanges** mediante KEEP_OPEN_READONLY establecido en  _ulFlags_.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si recibe la marca KEEP_OPEN_READONLY, tiene la opción de dejar el acceso del objeto como lectura y escritura. Sin embargo, un proveedor nunca puede dejar un objeto en un estado de solo lectura cuando se pasa KEEP_OPEN_READWRITE marca.
  
Cuando un cliente guarda varios datos adjuntos en varios mensajes, llama al **método SaveChanges** para cada dato adjunto y cada mensaje. A menudo, los clientes MAPI_DEFERRED_ERRORS para cada una de estas llamadas excepto para la última. Puede devolver errores con la última llamada o con llamadas anteriores. Incluso puede omitir la marca. 
  
Si KEEP_OPEN_READWRITE o KEEP_OPEN_READONLY se establece junto con MAPI_DEFERRED_ERRORS, puede omitir la solicitud de aplazamiento de error. Si MAPI_DEFERRED_ERRORS está establecido en _ulFlags_, se puede devolver uno de los errores diferidos anteriormente para la **llamada SaveChanges.** 
  
Si un proveedor de transporte remoto proporciona una implementación funcional de este método es opcional y depende de otras opciones de diseño en la implementación. Si implementa este método, hacerlo de acuerdo con la documentación aquí. Dado que los objetos de carpeta y los objetos de estado no se realizan transacciones, como mínimo, la implementación de **SaveChanges** por parte de un proveedor de transporte remoto debe devolver S_OK sin realizar ningún trabajo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si un cliente pasa KEEP_OPEN_READONLY, llama al método [IMAPIProp::SetProps](imapiprop-setprops.md) y, a continuación, vuelve a llamar a **SaveChanges,** puede producirse un error en la misma implementación. 
  
Después de recibir MAPI_E_NO_ACCESS de una llamada en la que KEEP_OPEN_READWRITE, seguirá teniendo permiso de lectura y escritura en el objeto. Puede volver a **llamar a SaveChanges,** pasando la marca KEEP_OPEN_READONLY o ninguna marca con KEEP_OPEN_SUFFIX. 
  
Si un proveedor admite la marca KEEP_OPEN_READWRITE depende de la implementación del proveedor. 
  
Para indicar que la única llamada que se realiza en el objeto después de **SaveChanges** es **IUnknown::Release**, no establezca ninguna marca para el _parámetro ulFlags._ Un error de **SaveChanges** indica que no se pudieron hacer los cambios pendientes permanentes. Diferentes proveedores controlan la ausencia de marcas en la **llamada SaveChanges** de forma diferente. Algunos proveedores tratan este estado del mismo modo que KEEP_OPEN_READONLY; otros proveedores lo interpretan igual que KEEP_OPEN_READWRITE. Aún así, otros proveedores cierran el objeto cuando no reciben marcas en la **llamada SaveChanges.** 
  
Algunas propiedades, normalmente las propiedades calculadas, no se pueden procesar hasta que se llama a **SaveChanges** y, en algunos casos, **a Release**.
  
Al realizar cambios masivos, como guardar datos adjuntos en varios mensajes, aplazar el procesamiento de errores estableciendo la marca MAPI_DEFERRED_ERRORS en  _ulFlags_. Si guarda varios datos adjuntos en varios mensajes, realice una llamada **a SaveChanges** a cada dato adjunto y una llamada **a SaveChanges** a cada mensaje. Establezca la MAPI_DEFERRED_ERRORS para cada llamada de datos adjuntos y para todos los mensajes excepto para la última. 
  
Si **SaveChanges** devuelve MAPI_E_OBJECT_CHANGED, compruebe si el objeto original se ha modificado. Si es así, advierte al usuario, que puede solicitar que los cambios sobrescriban los cambios anteriores o guarde el objeto en otro lugar. Si el objeto original se ha eliminado, advierte al usuario que le dé la oportunidad de guardar el objeto en otra ubicación. 
  
No puede llamar a **SaveChanges** con la FORCE_SAVE en un objeto abierto que se ha eliminado. 
  
Si **SaveChanges** devuelve un error, el objeto cuyos cambios se iban a guardar permanece abierto, independientemente de las marcas establecidas en el _parámetro ulFlags._ 
  
> [!IMPORTANT]
> Es posible que NON_EMS_XP_SAVE y SPAMFILTER_ONSAVE  _ulFlags_ no se definan en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con los siguientes valores: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Para obtener más información, vea [Saving MAPI Properties](saving-mapi-properties.md).
  
## <a name="see-also"></a>Vea también



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Guardar propiedades MAPI](saving-mapi-properties.md)

