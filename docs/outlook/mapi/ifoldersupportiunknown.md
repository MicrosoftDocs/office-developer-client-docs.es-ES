---
title: IUnknown A ifoldersupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351390"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información acerca de la compatibilidad de una carpeta con el uso compartido.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |Proveedor de almacenamiento de mensajes  <br/> |
|Identificador de interfaz:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtiene información sobre la compatibilidad de una carpeta con el uso compartido.  <br/> |
   
## <a name="remarks"></a>Comentarios

Por lo general, Microsoft Office Outlook requiere un proveedor de almacén MAPI para implementar esta interfaz si el proveedor desea compartir una carpeta. La excepción es el proveedor del almacén de Exchange Server, que puede compartir carpetas sin implementar esta interfaz.
  
Un cliente puede consultar un **[IMAPIFolder](imapifolderimapicontainer.md)** de **a ifoldersupport**. Si se realiza correctamente, llame a **a ifoldersupport:: GetSupportMask** y compruebe el bit **FS_SUPPORTS_SHARING** que se va a establecer. 
  

