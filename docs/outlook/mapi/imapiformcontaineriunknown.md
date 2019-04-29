---
title: IUnknown IMAPIFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407532"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Administra formularios en bibliotecas de formularios. Esta interfaz se usa para crear bibliotecas de formularios específicas de la aplicación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Expuesto por:  <br/> |Objetos de contenedor de formulario  <br/> |
|Implementado por:  <br/> |Proveedores de bibliotecas de formularios  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormContainer  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Instala un formulario en un contenedor de formulario.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Quita un formulario determinado de un contenedor de formularios.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Resuelve una clase de mensaje en su formulario en un contenedor de formularios y devuelve un objeto de información de formulario para ese formulario.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Resuelve un grupo de clases de mensaje en sus formularios en un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Devuelve una matriz de las propiedades utilizadas por todos los formularios instalados en un contenedor de formularios.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Devuelve el nombre para mostrar de un contenedor de formulario.  <br/> |
|[Volvió](imapiformcontainer-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de contenedor de formulario.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

