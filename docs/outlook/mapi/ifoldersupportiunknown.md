---
title: IFolderSupport IUnknown
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
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817220"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Proporciona información sobre la compatibilidad de una carpeta para compartir.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |Proveedor de almacén de mensajes  <br/> |
|Identificador de interfaz:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtiene información sobre la compatibilidad de una carpeta para compartir.  <br/> |
   
## <a name="remarks"></a>Comentarios

Por lo general, Microsoft Office Outlook requiere una MAPI proveedor para implementar esta interfaz si desea que el proveedor compartir una carpeta de almacén. La excepción es el proveedor de almacén de Exchange Server, que puede compartir carpetas sin tener que implementar esta interfaz.
  
Un cliente puede consultar un **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**. Si se realiza correctamente, llame a **IFolderSupport::GetSupportMask** y compruebe si el bit **FS_SUPPORTS_SHARING** va a establecer. 
  

