---
title: Mantenimiento de una biblioteca de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298463"
---
# <a name="maintaining-a-form-library"></a>Mantenimiento de una biblioteca de formularios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una biblioteca de formularios contiene toda la información importante sobre un formulario: sus propiedades, sus verbos y los archivos ejecutables del servidor. Algunos clientes permiten a los usuarios mantener, instalar o quitar servidores de formularios. Si desea ofrecer esta característica a los usuarios, debe tener acceso a:
  
- El archivo de configuración del servidor de formularios, un archivo con el. CFG.
    
- Objeto Container de la biblioteca de formularios, un objeto que implementa la interfaz [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) . 
    
Para tener acceso al archivo de configuración o a un directorio, use los medios que sean convenientes. Normalmente, los clientes presentan al usuario un cuadro de diálogo para instalar y quitar servidores de formularios que también se pueden usar para solicitar al usuario la ubicación del archivo de configuración.
  
Para tener acceso al contenedor de la biblioteca de formularios, llame al método [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) del administrador de formularios. Pase un valor de enumeración para especificar la biblioteca de formularios que se va a abrir y, si es necesario, un puntero al objeto que debe usar el administrador de formularios para abrir la biblioteca de formularios. Por ejemplo, si abre una biblioteca de [formularios de carpetas](folder-form-libraries.md), pase un puntero [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) . 
  
Una vez que **OpenFormContainer** devuelve el puntero **IMAPIFormContainer** , llame a [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) o [IMAPIFormContainer:: RemoveForm](imapiformcontainer-removeform.md), según el mantenimiento que se vaya a realizar. **InstallForm** agrega un servidor de formularios a la biblioteca; **RemoveForm** elimina un servidor de formularios de la biblioteca. 
  

