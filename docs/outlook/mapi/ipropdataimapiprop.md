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
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435148"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona la capacidad de recuperar y cambiar el acceso de las propiedades de un objeto. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Expuesto por:  <br/> |Objeto de datos de propiedad  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios y aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIPropData  <br/> |
|Tipo de puntero:  <br/> |LPPROPDATA  <br/> |
|Modelo de transacción:  <br/> |Notransacted  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Establece el nivel de acceso para el objeto.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Establece el nivel de acceso y el estado de una o varias de las propiedades del objeto.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Recupera el nivel de acceso y el estado de una o varias de las propiedades del objeto.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Agrega una o varias propiedades de tipo PT_OBJECT al objeto.  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI implementa la interfaz **IPropData::IMAPIProp** y la usan principalmente los proveedores de servicios que tienen acceso a esta implementación llamando a la [función CreateIProp.](createiprop.md) 
  
Para obtener más información acerca de los niveles de acceso en objetos y propiedades, vea [Permisos para objetos y propiedades](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

