---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411277"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] Recuento de los bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada de una plantilla para crear nuevas entradas de un tipo determinado. 
    
 _ulCreateFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se realiza la creación de entradas. Se pueden establecer las siguientes marcas:
    
CREATE_CHECK_DUP_LOOSE 
  
> Debe realizarse un nivel suelto de comprobación de entradas duplicadas. La implementación de la comprobación de entradas duplicadas sueltos es específica del proveedor. Por ejemplo, un proveedor puede definir una coincidencia libre como cualquier dos entradas que tengan el mismo nombre para mostrar.
    
CREATE_CHECK_DUP_STRICT 
  
> Debe realizarse un nivel estricto de comprobación de entradas duplicadas. La implementación de comprobación estricta de entradas duplicadas es específica del proveedor. Por ejemplo, un proveedor puede definir una coincidencia estricta como cualquier dos entradas que tengan el mismo nombre para mostrar y la misma dirección de mensajería.
    
CREATE_REPLACE 
  
> Una nueva entrada debe reemplazar una existente si se determina que las dos son duplicadas.
    
 _lppMAPIPropEntry_
  
> [salida] Puntero a un puntero a la entrada recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva entrada se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IABContainer::CreateEntry** crea una nueva entrada de un tipo determinado en el contenedor especificado y devuelve un puntero a una implementación de interfaz para obtener más acceso a la entrada. La nueva entrada se crea mediante una plantilla que se ha seleccionado en la lista de plantillas disponibles del contenedor publicada en su tabla de uso único. Los autores de llamadas tienen acceso a la tabla de uso único de un contenedor llamando a su método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitando la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Todos los contenedores que admiten **el método IABContainer::CreateEntry** deben ser modificables. Establece la marca de AB_MODIFIABLE contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable. 
  
Debe admitir todas las marcas _ulCreateFlags._ Sin embargo, la interpretación y el uso de estas marcas es específico de la implementación; es decir, puedes determinar qué significa la semántica de CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de la implementación. Si no puede o no determina si una entrada es duplicada, permita siempre la creación de la entrada. 
  
Algunos proveedores implementan una comprobación de entrada estricta al hacer coincidir el nombre para mostrar, la dirección de mensajería y la clave de búsqueda de una entrada; otros proveedores limitan la coincidencia con el nombre para mostrar y la dirección. La comprobación de entrada suelto se suele implementar comprobando solo el nombre para mostrar. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Notas a los implementadores del proveedor de libretas de direcciones de host

Si el contenedor puede crear entradas a partir de las plantillas de otros proveedores, la implementación de **CreateEntry** debe proporcionar almacenamiento para algunas o todas las propiedades asociadas con las entradas creadas. Por ejemplo, si proporciona almacenamiento para la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)de una entrada, puede generar su cuadro de diálogo de detalles sin tener que depender del proveedor externo. 
  
Si el contenedor puede crear entradas que admitan **la propiedad PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), la implementación de **CreateEntry** debe hacer lo siguiente: 
  
1. Llame al [método IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md) **OpenTemplateID permite** que el código del proveedor externo para la entrada se enlace a la nueva entrada que se está creando. Los proveedores externos admiten este proceso de enlace para mantener el control sobre las entradas creadas a partir de sus plantillas en los contenedores de proveedores de libretas de direcciones host. 
    
2. Realice cualquier inicialización necesaria y rellene el nuevo objeto con todas las propiedades de la entrada en el proveedor externo que el objeto devolvió en el parámetro  _lppMAPIPropNew_ de **OpenTemplateID**.
    
Si **OpenTemplateID** se realiza correctamente, copie las propiedades en la implementación a la que apunta el parámetro _lppMAPIPropNew_ en lugar de directamente a la implementación a la que apunta el parámetro _lpMAPIPropData._ Inicialice la nueva entrada para su uso sin conexión como lo haría con cualquier otra entrada de un proveedor externo. 
  
Si **OpenTemplateID devuelve** un error, **CreateEntry** debe producir un error. No permitir la creación de la entrada. Dado que el proveedor externo puede hacer suposiciones sobre los datos del proveedor, no cree una entrada con un identificador de plantilla que no se haya enlazado correctamente al proveedor externo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando **CreateEntry** devuelve, es posible que pueda o no tener acceso inmediatamente al identificador de entrada de la nueva entrada. Algunos proveedores de libretas de direcciones no lo hacen disponible hasta después de llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nueva entrada. 
  
Aunque las marcas de comprobación duplicadas se pasan como parámetros a **CreateEntry,** la operación de comprobación duplicada no se realiza hasta que se llama a **SaveChanges.** Por lo tanto, **SaveChanges** devuelve los errores relacionados, como MAPI_E_COLLISION, que indica que se ha intentado crear una entrada ya existente, en lugar de **CreateEntry**.
  
## <a name="see-also"></a>Consulte también



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

