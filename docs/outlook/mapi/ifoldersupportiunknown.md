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
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415778"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información sobre la compatibilidad de una carpeta para compartir.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |Proveedor de almacenamiento de mensajes  <br/> |
|Identificador de interfaz:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtiene información sobre la compatibilidad de una carpeta para compartir.  <br/> |
   
## <a name="remarks"></a>Comentarios

Por lo general, Microsoft Office Outlook un proveedor de almacén MAPI para implementar esta interfaz si el proveedor desea compartir una carpeta. La excepción es el Exchange Server de almacenamiento, que puede compartir carpetas sin implementar esta interfaz.
  
Un cliente puede consultar un **[IMAPIFolder](imapifolderimapicontainer.md)** para **IFolderSupport**. Si esto se realiza correctamente, llame a **IFolderSupport::GetSupportMask** y compruebe si se **FS_SUPPORTS_SHARING** bit que se va a establecer. 
  

