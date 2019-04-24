---
title: Carpetas de b�squeda MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: c1d7f67458852319587d98831d031b2c3a131871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357676"
---
# <a name="mapi-search-folders"></a>Carpetas de b�squeda MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria�� rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed. 
  
 **SetSearchCriteria** identifies the messages that match the specified restriction. The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder. When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table. Contents tables for search-results folders contain the same columns as contents tables for generic folders. Sin embargo, para las carpetas de resultados de búsqueda, la propiedad **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) especifica el identificador de entrada de la carpeta en la que reside el mensaje vinculado. Search-results folders are not considered parent folders.
  
Las carpetas de resultados de b�squeda tienen los siguientes l�mites:
  
- La �nica forma de que se puede modificar el contenido de una carpeta de resultados de b�squeda es a trav�s de una llamada a **SetSearchCriteria**. Para obtener m�s informaci�n acerca de la implementaci�n de **SetSearchCriteria**, vea el art�culo de Knowledge Base [260322: c�mo a las carpetas de b�squeda con el m�todo es posible SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).
    
- Los mensajes no se va a mover o copiar en carpetas de resultados de b�squeda.
    
- Las carpetas de resultados de b�squeda no pueden contener subcarpetas. 
    
- Los clientes no pueden realizar el asunto de una b�squeda de una carpeta de resultados de b�squeda.
    
Sin embargo, es posible modificar las propiedades de una carpeta de resultados de b�squeda y usarlo para eliminar un mensaje. Cuando se elimina un mensaje de una carpeta de resultados de b�squeda, se elimine realmente desde la carpeta real. Sin embargo, al eliminar la carpeta de resultados de b�squeda propio no influye en los mensajes dentro; permanecen en sus carpetas gen�ricos.
  
## <a name="see-also"></a>Vea también



[Carpetas de MAPI](mapi-folders.md)

