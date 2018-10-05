---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382949"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Copia las entradas de uno o más, los usuarios normalmente mensajería o listas de distribución.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpEntries_
  
> [entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que contiene los identificadores de entrada de las entradas para copiar. 
    
 _ulUIParam_
  
> [entrada] El identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método. El parámetro _ulUIParam_ debe ser cero si se establece la marca AB_NO_DIALOG en el parámetro _ulFlags indicado_ . 
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso o NULL. Si _lpProgress_ es NULL, se debe mostrar un indicador de progreso con el objeto de progreso proporcionado por MAPI a través del método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) . El parámetro _lpProgress_ se omite si se establece la marca AB_NO_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se realiza la operación de copia. Se pueden establecer los siguientes indicadores:
    
AB_NO_DIALOG 
  
> Suprime la visualización de un indicador de progreso. Si no se establece este marcador, se muestra un indicador de progreso.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indica que se debe realizar un nivel separado de comprobación de la entrada duplicada. La implementación de comprobación de la entrada duplicada suelto es específico del proveedor. Por ejemplo, un proveedor puede definir a una coincidencia separada como las dos entradas que tienen el mismo nombre para mostrar.
    
CREATE_CHECK_DUP_STRICT 
  
> Indica que se debe realizar un nivel estricto de comprobación de la entrada duplicada. La implementación de comprobación estricta entrada duplicada es específico del proveedor. Por ejemplo, un proveedor puede definir a una coincidencia estricta como las dos entradas que tienen ambos el mismo nombre para mostrar y la dirección de mensajería.
    
CREATE_REPLACE 
  
> Indica que una nueva entrada debe reemplazar uno existente si se determina que las dos son duplicados.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha realizado correctamente la operación de copia.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La operación de copia satisfactoria, pero no se podrían copiar uno o más de las entradas. Cuando se devuelve este valor, la llamada se debe controlarse como correcta. Para probar este valor, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IABContainer::CopyEntries** copia entradas desde el mismo contenedor o un contenedor diferente. Una llamada a **CopyEntries** es funcionalmente equivalente a hacer que las llamadas siguientes para cada entrada que se va a copiar: 
  
1. El método [IABContainer::CreateEntry](iabcontainer-createentry.md) para crear la nueva entrada. 
    
2. El método [IMAPIProp::GetProps](imapiprop-getprops.md) para leer las propiedades de la entrada que se va a copiar. 
    
3. El método [IMAPIProp::SetProps](imapiprop-setprops.md) para escribir las propiedades para la nueva entrada. 
    
4. [IMAPIProp::SaveChanges](imapiprop-savechanges.md) (método) de la nueva entrada para llevar a cabo un proceso de guardar. 
    
5. [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) (método) de la nueva entrada para liberar la referencia del contenedor. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Todos los contenedores que admiten el método **IABContainer::CopyEntries** deben ser modificables. Establecer marca AB_MODIFIABLE de su contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable. 
  
Debe admitir todas las marcas; Sin embargo, la interpretación y el uso de estos indicadores es específico de la implementación, es decir, puede determinar el significado de la semántica de los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de su implementación. Si no puede o no determinar si una entrada es un duplicado, permitir siempre la entrada que se va a copiar. 
  
Si se establece la marca CREATE_REPLACE, copie siempre la entrada, independientemente de si se ha establecido CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT y si la entrada es un duplicado. 
  
Si no se ha establecido CREATE_REPLACE y CREATE_CHECK_DUP_STRICT se establece, compruebe si existen duplicados. Si una entrada se determina como un duplicado, no copie la entrada. 
  
No es necesario admitir CREATE_REPLACE; no se admite la CREATE_REPLACE significa que puede omitir de forma segura y siempre realizar una copia. 
  
Devolver la advertencia MAPI_W_PARTIAL_COMPLETION sólo si no se puede copiar una entrada no duplicada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Utilice los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT para indicar al proveedor de cómo desea que el contenedor para realizar la comprobación de entrada de duplicado. Si necesita tener una entrada agregada independientemente de que sea un duplicado, no configure cualquiera de estos marcadores o establecer la marca CREATE_REPLACE. CREATE_REPLACE indica que no importa si una entrada es un duplicado; siempre que desea reemplazar la entrada original. 
  
## <a name="see-also"></a>Vea también



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

