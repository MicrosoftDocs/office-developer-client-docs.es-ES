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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346399"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia una o más entradas, normalmente usuarios de mensajería o listas de distribución.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpEntries_
  
> [in] Puntero a una matriz de [estructuras ENTRYLIST](entrylist.md) que contiene los identificadores de entrada de las entradas que se copian. 
    
 _ulUIParam_
  
> [in] El identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método. El _parámetro ulUIParam_ debe ser cero si la marca AB_NO_DIALOG se establece en el _parámetro ulFlags._ 
    
 _lpProgress_
  
> [in] Puntero a un objeto de progreso que muestra un indicador de progreso o NULL. Si _lpProgress_ es NULL, se debe mostrar un indicador de progreso mediante el objeto de progreso proporcionado por MAPI a través del método [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) El  _parámetro lpProgress_ se omite si la marca AB_NO_DIALOG se establece en  _ulFlags_.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se realiza la operación de copia. Se pueden establecer las siguientes marcas:
    
AB_NO_DIALOG 
  
> Suprime la presentación de un indicador de progreso. Si no se establece esta marca, se muestra un indicador de progreso.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indica que debe realizarse un nivel suelto de comprobación de entrada duplicada. La implementación de la comprobación de entrada duplicada suelta es específica del proveedor. Por ejemplo, un proveedor puede definir una coincidencia suelta como cualquier dos entradas que tengan el mismo nombre para mostrar.
    
CREATE_CHECK_DUP_STRICT 
  
> Indica que se debe realizar un nivel estricto de comprobación de entrada duplicada. La implementación de la comprobación estricta de entradas duplicadas es específica del proveedor. Por ejemplo, un proveedor puede definir una coincidencia estricta como cualquiera de las dos entradas que tienen el mismo nombre para mostrar y la misma dirección de mensajería.
    
CREATE_REPLACE 
  
> Indica que una nueva entrada debe reemplazar una existente si se determina que los dos son duplicados.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de copia se ha correcto.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La operación de copia se ha hecho correctamente en general, pero no se pudo copiar una o varias de las entradas. Cuando se devuelve este valor, la llamada debe controlarse como correcta. Para probar este valor, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IABContainer::CopyEntries** copia entradas del mismo contenedor o de un contenedor diferente. Una llamada a **CopyEntries** es funcionalmente equivalente a realizar las siguientes llamadas para cada entrada que se va a copiar: 
  
1. El [método IABContainer::CreateEntry](iabcontainer-createentry.md) para crear la nueva entrada. 
    
2. El [método IMAPIProp::GetProps](imapiprop-getprops.md) para leer las propiedades de la entrada que se va a copiar. 
    
3. El [método IMAPIProp::SetProps](imapiprop-setprops.md) para escribir propiedades en la nueva entrada. 
    
4. Método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nueva entrada para realizar un guardado. 
    
5. El método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) de la nueva entrada para liberar la referencia del contenedor. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Todos los contenedores que admiten **el método IABContainer::CopyEntries** deben ser modificables. Establezca la marca de AB_MODIFIABLE contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable. 
  
Debe admitir todas las marcas; sin embargo, la interpretación y el uso de estas marcas es específico de la implementación, es decir, puede determinar lo que significa la semántica de las marcas CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de la implementación. Si no puede o no determinar si una entrada es un duplicado, permita siempre que se copie la entrada. 
  
Si se CREATE_REPLACE marca, copie siempre la entrada independientemente de si CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT está establecida y si la entrada es un duplicado. 
  
Si CREATE_REPLACE está establecido y CREATE_CHECK_DUP_STRICT, compruebe si hay duplicados. Si se determina que una entrada es un duplicado, no copie la entrada. 
  
No es necesario que admita CREATE_REPLACE; no admitir CREATE_REPLACE significa que puede ignorarlo de forma segura y realizar siempre una copia. 
  
Devuelve la advertencia MAPI_W_PARTIAL_COMPLETION solo si no se puede copiar una entrada no duplicada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Use las CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT para indicar al proveedor cómo desea que el contenedor realice la comprobación de entrada duplicada. Si necesita agregar una entrada independientemente de si se trata de un duplicado, no establezca ninguna de estas marcas ni establezca la marca CREATE_REPLACE. CREATE_REPLACE indica que no le importa si una entrada es un duplicado; siempre desea que reemplace la entrada original. 
  
## <a name="see-also"></a>Vea también



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

