---
title: Instalar un formulario en una biblioteca
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433146"
---
# <a name="installing-a-form-into-a-library"></a>Instalar un formulario en una biblioteca

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El administrador de formularios MAPI predeterminado que se proporciona con Windows SDK no proporciona una interfaz de usuario para la instalación de formularios en las distintas bibliotecas de formularios. Por este motivo, tendrá que crear una aplicación pequeña (o un conjunto detallado de instrucciones) que los usuarios puedan usar para instalar el formulario.
  
Si implementa una aplicación de instalación, la serie de acciones que debe realizar para instalar un formulario en la tabla de contenido asociada a una carpeta es la siguiente:
  
1. Llame a la función [MAPIOpenFormMgr](mapiopenformmgr.md) para abrir el administrador de formularios. 
    
2. Use el método [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) o [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) para seleccionar y abrir el contenedor de destino del formulario. 
    
3. Use la función [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) para instalar el formulario. 
    
    Los pasos 4 a 6 son para la instalación en una biblioteca de formularios local:
    
4. Copie todos los archivos en el punto adecuado del disco local, si la instalación se realiza en la biblioteca de formularios local de la estación de trabajo del usuario. Si es necesario, modifique el archivo de configuración del formulario para reflejar las rutas de componentes actuales. El archivo de configuración de formulario puede contener rutas relativas, en cuyo caso es posible que este paso no sea necesario.
    
5. Complete los pasos de registro OLE apropiados para asociar el tipo de mensaje al servidor de formularios que se va a instalar.
    
6. Si el formulario se ha instalado en la biblioteca de formularios local, copie los archivos de icono (. ico) y de configuración (. cfg) del formulario en el directorio%WINDOWS%\FORMS\CONFIGS de manera que el formulario pueda restaurarse automáticamente en caso de que la biblioteca de formularios esté dañada o eliminada. Se recomienda este paso, pero no es obligatorio.
    
> [!NOTE]
> Puede simplificar la instalación en una biblioteca de formularios local si reemplaza los pasos 1 y 2 con una llamada a la función [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . 
  
## <a name="see-also"></a>Ver también



[Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

