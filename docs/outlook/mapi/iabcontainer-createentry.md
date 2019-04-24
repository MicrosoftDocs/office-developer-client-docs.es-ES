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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287031"
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> a El número de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada de una plantilla para crear nuevas entradas de un tipo determinado. 
    
 _ulCreateFlags_
  
> a Una máscara de máscara de marcas que controla cómo se realiza la creación de la entrada. Se pueden establecer los siguientes indicadores:
    
CREATE_CHECK_DUP_LOOSE 
  
> Debe realizarse un nivel flexible de comprobación de entrada duplicada. La implementación de la comprobación de entradas duplicadas perdidas es específica del proveedor. Por ejemplo, un proveedor puede definir una coincidencia perdida como dos entradas que tienen el mismo nombre para mostrar.
    
CREATE_CHECK_DUP_STRICT 
  
> Debe realizarse un nivel estricto de comprobación de entrada duplicada. La implementación de una comprobación de entrada de duplicados estrictas es específica del proveedor. Por ejemplo, un proveedor puede definir una coincidencia estricta como dos entradas que tienen el mismo nombre para mostrar y la misma dirección de mensajería.
    
CREATE_REPLACE 
  
> Una nueva entrada debe reemplazar A una existente si se determina que los dos son duplicados.
    
 _lppMAPIPropEntry_
  
> contempla Un puntero a un puntero a la entrada recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva entrada se ha creado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IABContainer:: CreateEntry** crea una nueva entrada de un tipo determinado en el contenedor especificado, que devuelve un puntero a una implementación de interfaz para obtener más acceso a la entrada. La nueva entrada se crea con una plantilla que se ha seleccionado a partir de la lista de plantillas disponibles publicadas en la tabla de un solo uso. Los llamadores obtienen acceso a la tabla única de un contenedor llamando a su método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) y solicitando la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Todos los contenedores que admiten el método **IABContainer:: CreateEntry** deben ser modificables. Establezca la marca AB_MODIFIABLE del contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable. 
  
Debe admitir todas las marcas _ulCreateFlags_ . Sin embargo, la interpretación y el uso de estas marcas son específicos de la implementación, es decir, puede determinar cuál es la semántica de CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de la implementación. Si no puede o no determina si una entrada es un duplicado, permita siempre que se cree la entrada. 
  
Algunos proveedores implementan la comprobación de entradas estrictas al hacer coincidir el nombre para mostrar, la dirección de mensajería y la clave de búsqueda en una entrada; otros proveedores limitan la coincidencia con el nombre para mostrar y la dirección. La comprobación de entradas perdidas se suele implementar comprobando solo el nombre para mostrar. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Notas para los implementadores del proveedor de la libreta de direcciones de host

Si el contenedor puede crear entradas de las plantillas de otros proveedores, la implementación de **CreateEntry** debe proporcionar almacenamiento para algunas o todas las propiedades asociadas con las entradas creadas. Por ejemplo, si proporciona almacenamiento para la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de una entrada, puede generar el cuadro de diálogo Detalles sin tener que depender del proveedor externo. 
  
Si el contenedor puede crear entradas que admiten la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), la implementación de **CreateEntry** debe hacer lo siguiente: 
  
1. Llame al método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) . **OpenTemplateID** permite que el código del proveedor externo para la entrada se enlace a la nueva entrada que se está creando. Los proveedores externos admiten este proceso de enlace para mantener el control sobre las entradas creadas a partir de sus plantillas en los contenedores de los proveedores de la libreta de direcciones de host. 
    
2. Realice las inicializaciones necesarias y rellene el objeto nuevo con todas las propiedades de la entrada en el proveedor externo que el objeto devuelto en el parámetro _lppMAPIPropNew_ de **OpenTemplateID**.
    
Si **OpenTemplateID** se ejecuta correctamente, copie las propiedades en la implementación señalada por el parámetro _lppMAPIPropNew_ en lugar de hacerlo directamente a la implementación señalada por el parámetro _lpMAPIPropData_ . Inicialice la nueva entrada para uso sin conexión como lo haría con cualquier otra entrada de un proveedor externo. 
  
Si **OpenTemplateID** devuelve un error, **CreateEntry** debe producirse un error. No permitir que se cree la entrada. Dado que el proveedor externo puede hacer suposiciones sobre los datos de su proveedor, no cree una entrada con un identificador de plantilla que no se haya enlazado correctamente al proveedor externo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando **CreateEntry** devuelve, es posible que no pueda obtener acceso inmediatamente al identificador de entrada de la nueva entrada. Algunos proveedores de libretas de direcciones no hacen que esté disponible hasta que se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la nueva entrada. 
  
Aunque las marcas de comprobación duplicadas se pasan como parámetros a **CreateEntry**, la operación de comprobación de duplicados no se produce hasta que se llama a **SaveChanges** . Por lo tanto, los errores relacionados, como MAPI_E_COLLISION, que indica que se ha realizado un intento de crear una entrada ya existente, son devueltos por **SaveChanges** en lugar de **CreateEntry**.
  
## <a name="see-also"></a>Vea también



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

