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
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321738"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona a las aplicaciones cliente acceso a las propiedades que son específicas de la definición del formulario. Al mantener la información del formulario en un objeto independiente, el proveedor de la biblioteca de formularios puede describir un formulario para un cliente sin activar el formulario.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Expuesto por:  <br/> |Objetos de información de formulario  <br/> |
|Implementado por:  <br/> |Proveedores de bibliotecas de formularios  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormInfo  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMINFO  <br/> |
|Modelo de transacción:  <br/> |No transactd  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Devuelve un puntero al conjunto completo de propiedades que usa un formulario.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Devuelve un puntero al conjunto completo de verbos que utiliza un formulario.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Crea un icono a partir de una propiedad Icon de un formulario.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Guarda una descripción de un formulario en particular en un archivo de configuración.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Devuelve un puntero al contenedor de formularios en el que se instala un formulario determinado.  <br/> |
   
## <a name="remarks"></a>Comentarios

A diferencia de la mayoría de las interfaces definidas en el archivo de encabezado MapiForm. h, **IMAPIFormInfo** hereda de la interfaz [IMAPIProp](imapipropiunknown.md) , porque exporta la mayoría de la información de formulario mediante llamadas al método [IMAPIProp:: GetProps](imapiprop-getprops.md) . 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

