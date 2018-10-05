---
title: Implementar la interfaz IClassFactory de servidores de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388052"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementar la interfaz IClassFactory de servidores de formulario

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) es la interfaz OLE que las aplicaciones cliente que se usan para crear nuevos objetos de formulario de clase de mensaje del servidor de su formulario. En la siguiente tabla se enumera los métodos de **IClassFactory** que son necesarios. 
  
|**Método**|**Descripción**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Crea un nuevo objeto de formulario.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Bloquea el servidor de formulario en la memoria para que se puede evitar la sobrecarga de inicio cuando se crean varios objetos de formulario.  <br/> |
   
Para toda la información necesaria para implementar estos métodos, vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows.
  
## <a name="see-also"></a>Vea también



[Escribir código de servidor de formulario](writing-form-server-code.md)

