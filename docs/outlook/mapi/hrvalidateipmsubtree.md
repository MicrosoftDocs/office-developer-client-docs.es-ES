---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436576"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega carpetas de mensaje interpersonal estándar (IPM) a un almacén de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Parameters

 _lpMDB_
  
> a Puntero al objeto de almacén de mensajes al que se van a agregar las carpetas. 
    
 _ulFlags_
  
> a Máscara de la máscara usada para controlar cómo se crean las carpetas. Se pueden establecer los siguientes indicadores:
    
MAPI_FORCE_CREATE 
  
> Las carpetas deben comprobarse antes de su creación, incluso si las propiedades del almacén de mensajes indican que son válidas. Una aplicación cliente normalmente establece esta marca cuando un error indica que la estructura de una carpeta existente está dañada. 
    
MAPI_FULL_IPM_TREE 
  
> El conjunto completo de carpetas IPM debe crearse en la carpeta raíz del almacén de mensajes. Los títulos de carpeta de la jerarquía son los siguientes:
    
    - Vistas de carpeta
    
    - Vistas comunes
    
    - Raíz de búsqueda\*
    
    - Subárbol IPM\*
    
    - Bandeja de entrada
    
    - Bandeja de salida
    
    - Elementos eliminados\*
    
    - Elementos enviados
    
    donde las tres carpetas marcadas \* con son el conjunto mínimo que se ha creado, incluso cuando no se ha establecido la marca MAPI_FULL_IPM_TREE. Una aplicación cliente normalmente establece esta marca cuando el almacén de mensajes en el que se van a crear las carpetas es el almacén predeterminado.
    
 _lpcValues_
  
> [in, out] Puntero al número de estructuras [SPropValue](spropvalue.md) que hay en la matriz devuelta en el parámetro _lppProps_ . El valor del parámetro _lpcValues_ puede ser cero si _lppProps_ es NULL. 
    
 _lppProps_
  
> [in, out] Puntero a un puntero a una matriz de estructuras **SPropValue** que contiene los valores de propiedad de la propiedad **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) y para las propiedades de identificador de entrada de carpeta apropiadas. Si **HrValidateIPMSubtree** crea una bandeja de entrada en el almacén de mensajes, la matriz **SPropValue** incluye un identificador de entrada de la bandeja de entrada con `PROP_TAG(PT_BINARY, PROP_ID_NULL)`una etiqueta de propiedad especial codificada como. El parámetro _lppProps_ puede ser null, que indica que la implementación de la llamada no requiere que se devuelva una matriz **SPropValue** . 
    
 _lppMapiError_
  
> contempla Puntero a un puntero a una estructura [MAPIERROR](mapierror.md) que contiene información sobre la versión, el componente y el contexto de un error. El parámetro _lppMAPIError_ se establece en NULL si no se devuelve ninguna estructura **MAPIERROR** . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

MAPI utiliza la función **HrValidateIPMSubtree** internamente para construir el subárbol estándar IPM en un almacén de mensajes cuando se abre por primera vez el almacén o cuando un almacén se convierte en el almacén predeterminado. Las aplicaciones cliente también pueden usar esta función para validar o reparar carpetas de mensajes estándar. 
  
 **HrValidateIPMSubtree** siempre crea las carpetas raíz de búsqueda y subárbol IPM en la carpeta raíz del almacén y en la carpeta elementos eliminados en la carpeta del subárbol IPM. La carpeta de subárbol IPM es la raíz de la jerarquía IPM en ese almacén de mensajes. La carpeta raíz de búsqueda se puede usar como la raíz de un subárbol para las carpetas de resultados de búsqueda. 
  
Los clientes IPM deben mostrar su vista de carpeta comenzando en la carpeta raíz del subárbol IPM y mostrando las carpetas secundarias debajo. La información de la carpeta raíz de un almacén de mensajes no debe aparecer en la interfaz de usuario de un cliente. Esta funcionalidad significa que si un cliente debe ocultar la información, la información se puede colocar en el directorio raíz del subárbol IPM, donde no es visible para el usuario. Por el contrario, las aplicaciones que no son de IPM y que requieren que los mensajes y las carpetas sean invisibles para el usuario, por ejemplo, en un almacén de mensajes basado en servidor, pueden colocarlas fuera de la jerarquía IPM. 
  
 **HrValidateIPMSubtree** establece la propiedad **PR_VALID_FOLDER_MASK** para indicar si cada carpeta IPM que crea tiene un identificador de entrada válido. Las siguientes propiedades de identificador de entrada del almacén de mensajes se establecen en los identificadores de entrada de las carpetas correspondientes y se devuelven en el parámetro _lppProps_ junto con **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Un marcador de posición [PROP_TAG](prop_tag.md) para la bandeja de entrada IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MstStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnValidateIPMSubtree  <br/> |MFCMAPI usa el método **HrValidateIPMSubtree** para agregar carpetas estándar a un almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

