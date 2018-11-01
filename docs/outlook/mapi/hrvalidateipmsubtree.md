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
ms.openlocfilehash: 2625b148d15c2f5ccf65eedf3a1b1f2c9d0d133e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592048"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Agrega las carpetas estándar de mensajes interpersonales (IPM) a un almacén de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
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

## <a name="parameters"></a>Parámetros

 _lpMDB_
  
> [entrada] Puntero al mensaje almacena el objeto que se va a agregar las carpetas. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para controlar cómo se crean las carpetas. Se pueden establecer los siguientes indicadores:
    
MAPI_FORCE_CREATE 
  
> Las carpetas deben comprobarse antes de la creación, incluso si las propiedades del almacén de mensajes indican que son válidos. Normalmente, una aplicación cliente establece esta marca cuando un error indica que se ha dañado la estructura de una carpeta existente. 
    
MAPI_FULL_IPM_TREE 
  
> El conjunto completo de carpetas IPM debe crearse en la carpeta raíz del almacén de mensajes. Los títulos de la carpeta en la jerarquía son:
    
    - Vistas de carpeta
    
    - Vistas comunes
    
    - Raíz de la búsqueda\*
    
    - Subárbol IPM\*
    
    - Bandeja de entrada
    
    - Bandeja de salida
    
    - Elementos eliminados\*
    
    - Elementos enviados
    
    donde las tres carpetas marcan con \* son el conjunto mínimo creado incluso cuando no se ha establecido el indicador MAPI_FULL_IPM_TREE. Normalmente, una aplicación cliente establece esta marca cuando el almacén de mensajes en el que son las carpetas que se creará es el almacén predeterminado.
    
 _lpcValues_
  
> [entrada, salida] Puntero al número de estructuras de [SPropValue](spropvalue.md) en la matriz devuelta en el parámetro _lppProps_ . El valor del parámetro _lpcValues_ puede ser cero si _lppProps_ es NULL. 
    
 _lppProps_
  
> [entrada, salida] Puntero a un puntero a una matriz de estructuras **SPropValue** que contiene los valores de propiedad para la propiedad **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) y de las propiedades de identificador de entrada de carpeta correspondiente. Si **HrValidateIPMSubtree** crea una bandeja de entrada en el almacén de mensajes, la matriz **SPropValue** incluye un identificador de entrada de la Bandeja de entrada con una etiqueta de propiedad especial de forma rígida como `PROP_TAG(PT_BINARY, PROP_ID_NULL)`. El parámetro _lppProps_ puede ser NULL, que indica que la implementación de la llamada no requiere que se devuelve una matriz de **SPropValue** . 
    
 _lppMapiError_
  
> [out] Puntero a un puntero a una estructura [MAPIERROR](mapierror.md) que contiene información de versión, el componente y el contexto de un error. El parámetro _lppMAPIError_ se establece en NULL si no hay estructura **MAPIERROR** se devuelve. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

MAPI utiliza la función **HrValidateIPMSubtree** internamente para construir el subárbol IPM estándar en un almacén de mensajes cuando se abre el almacén por primera vez o cuando un almacén se realiza almacenar el valor predeterminado. Esta función también puede utilizarse por las aplicaciones cliente para validar o reparar carpetas de mensajes estándar. 
  
 **HrValidateIPMSubtree** siempre crea las carpetas raíz de la búsqueda y subárbol IPM en la carpeta del almacén raíz y la carpeta Elementos eliminados en la carpeta subárbol IPM. La carpeta subárbol IPM es la raíz de la jerarquía de IPM de ese almacén de mensajes. La carpeta raíz de la búsqueda se puede usar como la raíz de un subárbol de carpetas de resultados de búsqueda. 
  
Los clientes IPM deben mostrar su vista de carpeta empezando en la carpeta raíz del subárbol IPM y mostrar a secundarios las carpetas por debajo de ella. Información de la carpeta raíz de un almacén de mensajes no debe aparecer en la interfaz de usuario de un cliente. Esta funcionalidad significa que si un cliente debe ocultar información, la información se puede poner en el directorio de raíz del subárbol IPM, donde no es visible para el usuario. Por el contrario, las aplicaciones que no sean IPM que requieren los mensajes y carpetas para ser invisibles para el usuario, por ejemplo en un almacén de mensajes basado en servidor, pueden ponerlos fuera de la jerarquía IPM. 
  
 **HrValidateIPMSubtree** establece la propiedad **PR_VALID_FOLDER_MASK** para indicar si cada carpeta IPM crea tiene un identificador de entrada válido. Las siguientes propiedades de identificador de entrada del almacén de mensajes se establece en los identificadores de entrada de las carpetas correspondientes y devuelven en el parámetro _lppProps_ junto con **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Un marcador de posición [PROP_TAG](prop_tag.md) para la Bandeja de entrada IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI utiliza el método **HrValidateIPMSubtree** para agregar carpetas estándar a un almacén de mensajes.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

