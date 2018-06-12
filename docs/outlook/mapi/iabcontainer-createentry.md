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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: acf9cee9bf0713b909b0d82fc606b015ac28474e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817108"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**Se aplica a**: Outlook 
  
Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a>Sintaxis

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicada por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de una plantilla para la creación de nuevas entradas de un tipo determinado. 
    
 _ulCreateFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la creación de entrada. Se pueden establecer los siguientes indicadores:
    
CREATE_CHECK_DUP_LOOSE 
  
> Debe realizar un nivel separado de comprobación de la entrada duplicada. La implementación de comprobación de la entrada duplicada suelto es específico del proveedor. Por ejemplo, un proveedor puede definir a una coincidencia separada como las dos entradas que tienen el mismo nombre para mostrar.
    
CREATE_CHECK_DUP_STRICT 
  
> Debe realizar un nivel estricto de comprobación de la entrada duplicada. La implementación de comprobación estricta entrada duplicada es específico del proveedor. Por ejemplo, un proveedor puede definir a una coincidencia estricta como las dos entradas que tienen ambos el mismo nombre para mostrar y la dirección de mensajería.
    
CREATE_REPLACE 
  
> Una nueva entrada debería reemplazar uno existente si se determina que las dos son duplicados.
    
 _lppMAPIPropEntry_
  
> [out] Un puntero a un puntero a la entrada recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado correctamente la nueva entrada.
    
## <a name="remarks"></a>Notas

El método **IABContainer::CreateEntry** crea una nueva entrada de un tipo determinado en el contenedor especificado, la devolución de un puntero a una implementación de la interfaz para obtener acceso a la entrada. La nueva entrada se crea mediante el uso de una plantilla que se ha seleccionado desde la lista del contenedor de plantillas disponibles publicado en su tabla de uso único. Los autores de llamadas tener acceso a la tabla de uso único de un contenedor llamando a su método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitar la propiedad de **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Todos los contenedores que admiten el método **IABContainer::CreateEntry** deben ser modificables. Establecer marca AB_MODIFIABLE de su contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable. 
  
Debe admitir todas las marcas de _ulCreateFlags_ . Sin embargo, la interpretación y el uso de estos indicadores es específico de la implementación, es decir, puede determinar el significado de la semántica de CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de su implementación. Si no puede o no determinar si una entrada es un duplicado, permitir siempre la entrada que se creará. 
  
Algunos proveedores de implementan la entrada estricta de comprobación de forma que coincida con el nombre para mostrar, mensajería dirección y la clave de búsqueda en una entrada; otros proveedores de limitan la coincidencia para mostrar el nombre y la dirección. A menudo se implementa la comprobación de entrada separado comprobando el nombre para mostrar sólo. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Notas para implementadores de proveedor de la libreta de direcciones de Host

Si el contenedor puede crear las entradas de las plantillas de otros proveedores, la implementación de **CreateEntry** debe proporcionar almacenamiento para algunas o todas las propiedades asociadas con los movimientos creados. Por ejemplo, si proporciona almacenamiento para la propiedad de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de la entrada, puede generar su cuadro de diálogo detalles sin tener que dependen del proveedor externo. 
  
Si el contenedor puede crear las entradas que admiten la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), la implementación de **CreateEntry** debe hacer lo siguiente: 
  
1. Llame al método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . **OpenTemplateID** permite que el código del proveedor externo para la entrada enlazar a la nueva entrada que se está creando. Proveedores de externos admiten este proceso de enlace para mantener el control sobre las entradas de creado a partir de sus plantillas en los contenedores de los proveedores de la libreta de direcciones de host. 
    
2. Realizar cualquier inicialización necesaria y rellenar el objeto nuevo con todas las propiedades de la entrada en el proveedor extranjero que devuelve el objeto en el parámetro _lppMAPIPropNew_ desde **OpenTemplateID**.
    
Si se realiza correctamente **OpenTemplateID** , copie las propiedades para la implementación indicada por el parámetro _lppMAPIPropNew_ en lugar de hacerlo directamente a la implementación que apunta el parámetro _lpMAPIPropData_ . Inicializar la nueva entrada para su uso sin conexión tal y como lo haría con cualquier otra entrada de un proveedor externo. 
  
Si **OpenTemplateID** devuelve un error, debe producirse un error en **CreateEntry** . No permitir la entrada que se creará. Debido a que el proveedor externo puede realizar suposiciones acerca de los datos de su proveedor, no cree una entrada con un identificador de plantilla que no se ha enlazado correctamente al proveedor externo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se devuelve **CreateEntry** , puede o no inmediatamente obtener acceso el identificador de entrada para la nueva entrada. Algunos proveedores de libreta de direcciones no permitir que esté disponible hasta después de llamar a (método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ) de la nueva entrada. 
  
Aunque los indicadores de comprobación duplicados se pasan como parámetros al **CreateEntry**, el duplicado en la operación de comprobación no se produce hasta que se llama **SaveChanges** . Por lo tanto, se devuelven errores relacionados, como MAPI_E_COLLISION, que indica que se ha intentado crear una entrada ya existente, por **SaveChanges** en lugar de **CreateEntry**.
  
## <a name="see-also"></a>Ver también



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Propiedad canónico PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)

