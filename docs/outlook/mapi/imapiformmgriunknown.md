---
title: IUnknown IMAPIFormMgr
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
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413062"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite a los visores de formulario obtener información acerca de los servidores de formularios y activarlos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Expuesto por:  <br/> |Objetos del administrador de formularios  <br/> |
|Implementado por:  <br/> |Proveedores de bibliotecas de formularios  <br/> |
|Llamado por:  <br/> |Visores de formularios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormMgr  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Inicia un formulario para abrir un mensaje existente.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Resuelve una clase de mensaje en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Resuelve un grupo de clases de mensaje en sus formularios dentro de un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Devuelve una matriz de las propiedades que utiliza un grupo de formularios.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Inicia un formulario para crear un nuevo mensaje basado en la clase de mensaje del formulario.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Muestra un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe dicho formulario.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de objetos de información de formulario que describen esos formularios.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formularios y devuelve una interfaz para el objeto contenedor seleccionado por el usuario.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Abre una interfaz [IMAPIFormContainer](imapiformcontaineriunknown.md) para un contenedor de formularios específico.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Descarga un formulario para abrirlo.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Determina si un formulario puede controlar sus propios conflictos de mensajes.  <br/> |
|[Volvió](imapiformmgr-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto administrador de formularios.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

