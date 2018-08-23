---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b4eaf424bd22f5cb7f40778d81a18cca0ef1dcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581520"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que los visores de formulario obtener información acerca de y activar servidores de formulario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Objetos de administrador de formulario  <br/> |
|Se implementa mediante:  <br/> |Proveedores de biblioteca de formulario  <br/> |
|Llamado por:  <br/> |Visores de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormMgr  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Inicia un formulario para abrir un mensaje existente.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Una clase de mensaje se resuelve en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Se resuelve un grupo de clases de mensajes en sus formularios dentro de un contenedor de formulario y devuelve una matriz de formulario objetos de información para los formularios.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Devuelve una matriz de las propiedades que utiliza un grupo de formularios.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Inicia un formulario para crear un nuevo mensaje en función de la clase de mensaje del formulario.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Presenta un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe ese formulario.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de formulario objetos de información que se describen dichos formularios.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto de contenedor seleccionado por el usuario.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Se abre una interfaz de [IMAPIFormContainer](imapiformcontaineriunknown.md) para un contenedor de forma específicos.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Descargas de un formulario para abrirlo.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Determina si un formulario puede controlar sus propio conflictos de mensaje.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen en el objeto de administrador de formulario.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

