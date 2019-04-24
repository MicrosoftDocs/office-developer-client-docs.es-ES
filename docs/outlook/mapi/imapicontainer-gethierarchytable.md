---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286942"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a la tabla de jerarquías del contenedor.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se devuelve la información en la tabla. Se pueden establecer los siguientes indicadores:
    
CONVENIENT_DEPTH 
  
> Rellena la tabla de jerarquía con contenedores de varios niveles. Si no se establece CONVENIENT_DEPTH, la tabla de jerarquías contiene sólo los contenedores secundarios inmediatos del contenedor.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** puede volver correctamente, posiblemente antes de que el autor de la llamada haya disponible la tabla. Si la tabla no está disponible, realizar una llamada subsiguiente a la tabla puede generar un error. 
    
MAPI_UNICODE 
  
> Solicita que las columnas que contienen datos de cadena se devuelvan en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas deben devolverse en formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, se encuentran en la fase de retención de elementos eliminados.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla de jerarquía.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de jerarquías se recuperó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El contenedor no tiene contenedores secundarios y no puede proporcionar una tabla de jerarquía.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer:: GetHierarchyTable** devuelve un puntero a la tabla de jerarquías de un contenedor. Una tabla de jerarquía contiene información de resumen sobre los contenedores secundarios del contenedor. Las tablas de jerarquía de carpetas contienen información acerca de las subcarpetas; las tablas de jerarquías de la libreta de direcciones contienen información sobre contenedores de libretas de direcciones secundarios y listas de distribución. 
  
Es posible que algunos contenedores no tengan contenedores secundarios. Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones de **GetHierarchyTable**.
  
Cuando se establece la marca CONVENIENT_DEPTH, cada fila de la tabla de jerarquía también incluye la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como una columna. **PR_DEPTH** indica el nivel de cada contenedor en relación con el contenedor que implementa la tabla. Los contenedores secundarios inmediatos del contenedor que se implementan están en cero de profundidad, los contenedores secundarios de los contenedores de profundidad cero están a la profundidad uno y así sucesivamente. Los valores de **PR_DEPTH** aumentan secuencialmente a medida que se profundiza en la jerarquía de niveles. 
  
Para obtener una lista completa de las columnas requeridas y opcionales de las tablas de jerarquía, consulte [Hierarchy tables](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si admite una tabla de jerarquías para el contenedor, también debe hacer lo siguiente:
  
- Admitir una llamada al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Devuelve **PR_CONTAINER_HIERARCHY** de una llamada a los métodos [IMAPIProp:: GetPropList](imapiprop-getproplist.md) o [IMAPIProp:: GetProps](imapiprop-getprops.md) del contenedor. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Las columnas de la tabla de contenido binario y de cadena pueden truncarse. Normalmente, los proveedores devuelven 255 caracteres. Como no se puede saber de antemano si una tabla incluye columnas truncadas, se supone que una columna está truncada si la longitud de la columna es de 255 o de 510 bytes. Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto mediante su identificador de entrada para abrirla y, a continuación, llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) . 
  
Según la implementación del proveedor, las restricciones y las operaciones de ordenación pueden aplicarse a toda la cadena o a la versión truncada de esa cadena. Además, no se garantiza que los proveedores de almacenamiento respeten el criterio de ordenación especificado en [SSortOrderSet](ssortorderset.md) para las tablas de jerarquía. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl. cpp  <br/> |CHierarchyTableTreeCtrl:: GetHierarchyTable  <br/> |La clase CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obtener las tablas de jerarquía que se mostrarán en un control de vista de árbol.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propiedad canónica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

