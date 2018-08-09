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
ms.openlocfilehash: 54b2dece31937b1ff233d4d1e7d8bbc198bfe118
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817836"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="12530-103">Instalar un formulario en una biblioteca</span><span class="sxs-lookup"><span data-stu-id="12530-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="12530-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12530-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12530-105">El Administrador de formularios MAPI predeterminada que se proporciona con el SDK de Windows no proporciona una interfaz de usuario para la instalación de formularios en las diversas bibliotecas de formulario.</span><span class="sxs-lookup"><span data-stu-id="12530-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="12530-106">Por este motivo, debe crear una aplicación pequeña: o detallada conjunto de instrucciones, que los usuarios pueden usar para instalar el formulario.</span><span class="sxs-lookup"><span data-stu-id="12530-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="12530-107">Si implementa una aplicación de instalación, la serie de acciones que debe realizar para instalar un formulario en contenido asociada de una carpeta tabla son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="12530-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="12530-108">Llame a la función [MAPIOpenFormMgr](mapiopenformmgr.md) para abrir el formulario de administrador.</span><span class="sxs-lookup"><span data-stu-id="12530-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="12530-109">Utilice el método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) o [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para seleccionar y abrir el contenedor de destino para el formulario.</span><span class="sxs-lookup"><span data-stu-id="12530-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="12530-110">Use la función [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) para instalar el formulario.</span><span class="sxs-lookup"><span data-stu-id="12530-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="12530-111">Son los pasos del 4 al 6 para su instalación en una biblioteca de formularios local:</span><span class="sxs-lookup"><span data-stu-id="12530-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="12530-112">Copie todos los archivos en el lugar adecuado en el disco local, si la instalación es para la biblioteca de formularios local en la estación de trabajo del usuario.</span><span class="sxs-lookup"><span data-stu-id="12530-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="12530-113">Si es necesario, modifique el archivo de configuración de formulario para reflejar las rutas de acceso actuales de los componentes.</span><span class="sxs-lookup"><span data-stu-id="12530-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="12530-114">El archivo de configuración de formulario puede contener rutas de acceso relativas, en cuyo caso este paso puede no ser necesario.</span><span class="sxs-lookup"><span data-stu-id="12530-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="12530-115">Complete los pasos de registro OLE apropiados para asociar el tipo de mensaje con el servidor de formulario que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="12530-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="12530-116">Si el formulario se ha instalado en la biblioteca de formularios local, copie el formulario icono (.ico) y los archivos de configuración (.cfg) en el directorio %WINDOWS%\FORMS\CONFIGS por lo que el formulario se puede restaurar automáticamente en caso de que la biblioteca de formularios se daña o se elimina.</span><span class="sxs-lookup"><span data-stu-id="12530-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="12530-117">Este paso es recomendable pero no obligatorio.</span><span class="sxs-lookup"><span data-stu-id="12530-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="12530-118">Puede simplificar la instalación a una biblioteca de formularios local mediante el reemplazo de los pasos 1 y 2 con una llamada a la función [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="12530-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12530-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="12530-119">See also</span></span>



[<span data-ttu-id="12530-120">Desarrollar servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="12530-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

