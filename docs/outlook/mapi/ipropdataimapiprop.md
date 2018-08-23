---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c320b2c42b9a14c6dc428fc3df59991528cdbe36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592573"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona la capacidad para recuperar y cambiar el acceso para las propiedades de un objeto. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Expuestos por:  <br/> |Objeto de datos (propiedad)  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios y aplicaciones de cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIPropData  <br/> |
|Tipo de puntero:  <br/> |LPPROPDATA  <br/> |
|Modelo de transacciones:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Establece el nivel de acceso para el objeto.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Establece el nivel de acceso y el estado de una o varias de las propiedades del objeto.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Recupera el nivel de acceso y el estado de una o varias de las propiedades del objeto.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Agrega una o más propiedades de tipo pt Object para el objeto.  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz de **IPropData::IMAPIProp** se implementa mediante MAPI y resultan de utilidad para los proveedores de servicios que tienen acceso a esta implementación mediante una llamada a la función [CreateIProp](createiprop.md) . 
  
Para obtener más información acerca de los niveles de acceso en los objetos y propiedades, vea [los permisos de objetos y propiedades](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

