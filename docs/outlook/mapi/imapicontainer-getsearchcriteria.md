---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412026"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene los criterios de búsqueda del contenedor.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Una máscara de bits de marcadores que controla el tipo de las cadenas pasadas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _lppRestriction_
  
> contempla Un puntero a un puntero a una estructura [SRestriction](srestriction.md) que define los criterios de búsqueda. Si una aplicación cliente pasa NULL en el parámetro _lppRestriction_ , **GetSearchCriteria** no devuelve una estructura **SRestriction** . 
    
 _lppContainerList_
  
> contempla Un puntero a un puntero a una matriz de identificadores de entrada que representan los contenedores que se van a incluir en la búsqueda. Si un cliente pasa NULL en el parámetro _lppContainerList_ , **GetSearchCriteria** no devuelve una matriz de identificadores de entrada. 
    
 _lpulSearchState_
  
> contempla Puntero a una máscara de máscara de marcas usada para indicar el estado actual de la búsqueda. Si un cliente pasa NULL en el parámetro _lpulSearchState_ , **GetSearchCriteria** no devuelve ningún marcador. Se pueden establecer los siguientes indicadores: 
    
SEARCH_FOREGROUND 
  
> La búsqueda debe ejecutarse con prioridad alta en relación con otras búsquedas. Si no se establece esta marca, la búsqueda se ejecuta con prioridad normal en relación con otras búsquedas.
    
SEARCH_REBUILD 
  
> La búsqueda está en el modo de uso intensivo de la CPU de su funcionamiento, lo que intenta encontrar los mensajes que coinciden con los criterios. Si no se establece esta marca, la parte que consume mucha CPU de la operación de búsqueda ha finalizado. Este indicador solo tiene significado si la búsqueda está activa (es decir, si se ha establecido la marca SEARCH_RUNNING).
    
SEARCH_RECURSIVE 
  
> La búsqueda está buscando en los contenedores especificados y en todos sus contenedores secundarios para las entradas coincidentes. Si no se establece esta marca, solo se busca en los contenedores incluidos explícitamente en la última llamada al método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) . 
    
SEARCH_RUNNING 
  
> La búsqueda está activa y la tabla de contenido del contenedor se está actualizando para reflejar los cambios en el almacén de mensajes o la libreta de direcciones. Si no se establece esta marca, la búsqueda está inactiva y la tabla de contenido es estática.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los criterios de búsqueda se obtuvieron correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Los criterios de búsqueda nunca se establecieron para el contenedor.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer:: GetSearchCriteria** obtiene los criterios de búsqueda de un contenedor que admite búsquedas, normalmente una carpeta de resultados de búsqueda. Los criterios de búsqueda se crean llamando al método **IMAPIContainer:: SetSearchCriteria** del contenedor. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Es posible que los contenedores de la libreta de direcciones solo deban admitir **GetSearchCriteria** si proporcionan las capacidades de búsqueda avanzada asociadas con la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Para obtener más información acerca de cómo implementar la característica de búsqueda avanzada para los contenedores de la libreta de direcciones, consulte [implementación de búsqueda avanzada](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando termine con las estructuras de datos a las que apuntan los parámetros _lppRestriction_ y _lppContainerList_ , llame a [MAPIFreeBuffer](mapifreebuffer.md) una vez para cada estructura que se va a liberar. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|HierarchyTableDlg. cpp  <br/> |CHierarchyTableDlg:: OnEditSearchCriteria  <br/> |MFCMAPI usa el método **IMAPIContainer:: GetSearchCriteria** para obtener los criterios de búsqueda de la carpeta que se va a mostrar.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

