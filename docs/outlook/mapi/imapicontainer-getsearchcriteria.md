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
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579966"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene los criterios de búsqueda para el contenedor.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas que se pasan en. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _lppRestriction_
  
> [out] Un puntero a un puntero a una estructura [SRestriction](srestriction.md) que define los criterios de búsqueda. Si una aplicación cliente pasa NULL en el parámetro _lppRestriction_ , **es posible GetSearchCriteria** no devuelve una estructura **SRestriction** . 
    
 _lppContainerList_
  
> [out] Un puntero a un puntero a una matriz de identificadores de entrada que representan los contenedores que se deben incluir en la búsqueda. Si un cliente pasa NULL en el parámetro _lppContainerList_ , **es posible GetSearchCriteria** no devuelve una matriz de identificadores de entrada. 
    
 _lpulSearchState_
  
> [out] Un puntero a una máscara de bits de indicadores que se utilizan para indicar el estado actual de la búsqueda. Si un cliente pasa NULL en el parámetro _lpulSearchState_ , **es posible GetSearchCriteria** no devuelve marcadores. Se pueden establecer los siguientes indicadores: 
    
SEARCH_FOREGROUND 
  
> La búsqueda debe ejecutarse con prioridad alta con respecto a otras búsquedas. Si no se establece este marcador, la búsqueda se ejecuta con prioridad normal con respecto a otras búsquedas.
    
SEARCH_REBUILD 
  
> La búsqueda está en el modo con uso intensivo de la CPU de su funcionamiento, intenta localizar los mensajes que coinciden con los criterios. Si no se establece este indicador, el elemento con uso intensivo de la CPU de la operación de búsqueda es a través de. Esta marca sólo tiene significado si está activa la búsqueda (es decir, si se establece la marca SEARCH_RUNNING).
    
SEARCH_RECURSIVE 
  
> La búsqueda está buscando en los contenedores especificados y todas sus contenedores secundarios para que coincidan con las entradas. Si no se establece este marcador, solo los contenedores que incluyen explícitamente en la última llamada al método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) se está buscando. 
    
SEARCH_RUNNING 
  
> La búsqueda está activa y se está actualizando la tabla de contenido del contenedor para reflejar los cambios en el almacén de mensajes o la libreta de direcciones. Si no se establece este marcador, la búsqueda está inactiva y la tabla de contenido es estática.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se obtuvo correctamente los criterios de búsqueda.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Criterios de búsqueda nunca se han establecido para el contenedor.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer::GetSearchCriteria** obtiene los criterios de búsqueda para un contenedor que admite búsquedas, normalmente una carpeta de resultados de búsqueda. Para crear criterios de búsqueda, llamar al método **IMAPIContainer::SetSearchCriteria** de un contenedor. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Contenedores de libretas de direcciones que necesite admitir **es posible GetSearchCriteria** sólo si se proporcionan las capacidades de búsqueda avanzada asociadas con la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Para obtener más información acerca de cómo implementar la característica de búsqueda avanzada para contenedores de la libreta de direcciones, vea [Implementación de búsqueda avanzada](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando haya terminado con las estructuras de datos indicadas por los parámetros _lppRestriction_ y _lppContainerList_ , llame a [MAPIFreeBuffer](mapifreebuffer.md) una vez para cada estructura que liberar. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI usa el método **IMAPIContainer::GetSearchCriteria** para obtener los criterios de búsqueda de una carpeta para mostrar.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

