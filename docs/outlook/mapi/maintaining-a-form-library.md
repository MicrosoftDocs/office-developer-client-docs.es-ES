---
title: Mantener una biblioteca de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5ccb5a2881d3cef3ff21a106e7e9ea33e0aedd9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818046"
---
# <a name="maintaining-a-form-library"></a>Mantener una biblioteca de formularios

  
  
**Hace referencia a**: Outlook 
  
Una biblioteca de formularios contiene toda la información importante acerca de un formulario: archivos ejecutables de su servidor, sus verbos y sus propiedades. Algunos clientes de que sus usuarios puedan mantener, instalar o quitar servidores de formulario. Si desea ofrecer esta característica a los usuarios, debe tener acceso a:
  
- Archivo de configuración del servidor de formulario, un archivo con el. Extensión CFG.
    
- Objeto de contenedor de la biblioteca de formularios, un objeto que implementa el [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interfaz. 
    
Para obtener acceso al archivo de configuración o una ruta de acceso a él, use cualquier medio es conveniente. Normalmente, los clientes de presentan al usuario un cuadro de diálogo para la instalación y eliminación de servidores de formulario que también pueden utilizarse para solicitar al usuario de la ubicación del archivo de configuración.
  
Para obtener acceso a contenedor de la biblioteca de formularios, llame al método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) del director de formulario. Pase un valor de enumeración para especificar qué biblioteca de formularios para abrir y si es necesario, un puntero al objeto que se debe usar el Administrador de formularios para abrir la biblioteca de formularios. Por ejemplo, si va a abrir una de [Las bibliotecas de formularios de carpeta](folder-form-libraries.md), pase una [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) puntero. 
  
Una vez **OpenFormContainer** devuelve el puntero **IMAPIFormContainer** , llame a [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) o [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), según el mantenimiento que se debe realizar. **InstallForm** agrega un servidor de formulario a la biblioteca; **RemoveForm** elimina un servidor de formulario de la biblioteca. 
  

