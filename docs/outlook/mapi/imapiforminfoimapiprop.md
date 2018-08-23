---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575913"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso de las aplicaciones de cliente a las propiedades que son específicas de la definición del formulario. Al mantener la información del formulario en un objeto independiente, el proveedor de la biblioteca de formulario puede describir un formulario a un cliente sin activar el formulario.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Objetos de información de formulario  <br/> |
|Se implementa mediante:  <br/> |Proveedores de biblioteca de formulario  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormInfo  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMINFO  <br/> |
|Modelo de transacciones:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Devuelve un puntero a todo el conjunto de propiedades que utiliza un formulario.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Devuelve un puntero a todo el conjunto de verbos que usa un formulario.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Se basa en un icono de una propiedad de icono de un formulario.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Guarda una descripción de un formulario determinado en un archivo de configuración.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Devuelve un puntero al contenedor de formulario en el que está instalado un formulario en particular.  <br/> |
   
## <a name="remarks"></a>Comentarios

A diferencia de la mayoría de las interfaces definida en el archivo de encabezado MapiForm.h, **IMAPIFormInfo** se hereda de la interfaz [IMAPIProp](imapipropiunknown.md) , debido a que exporta la mayoría información de formulario a través de las llamadas al método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

