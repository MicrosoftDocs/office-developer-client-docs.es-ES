---
title: Instalación de un formulario en una biblioteca
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
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="e8d37-103">Instalación de un formulario en una biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8d37-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="e8d37-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8d37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8d37-105">El administrador de formularios MAPI predeterminado proporcionado con el SDK de Windows no proporciona una interfaz de usuario para instalar formularios en las distintas bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="e8d37-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="e8d37-106">Debido a esto, tendrá que crear una aplicación pequeña (o un conjunto detallado de instrucciones) que los usuarios puedan usar para instalar el formulario.</span><span class="sxs-lookup"><span data-stu-id="e8d37-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="e8d37-107">Si implementa una aplicación de instalación, la serie de acciones que debe realizar para instalar un formulario en la tabla de contenido asociada de una carpeta son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8d37-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="e8d37-108">Llame a [la función MAPIOpenFormMgr](mapiopenformmgr.md) para abrir el administrador de formularios.</span><span class="sxs-lookup"><span data-stu-id="e8d37-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="e8d37-109">Use [el método IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) o [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para seleccionar y abrir el contenedor de destino del formulario.</span><span class="sxs-lookup"><span data-stu-id="e8d37-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="e8d37-110">Use la [función IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) para instalar el formulario.</span><span class="sxs-lookup"><span data-stu-id="e8d37-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="e8d37-111">Los pasos del 4 al 6 son para la instalación en una biblioteca de formularios local:</span><span class="sxs-lookup"><span data-stu-id="e8d37-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="e8d37-112">Copie todos los archivos en el lugar adecuado en el disco local, si la instalación es en la biblioteca de formularios local de la estación de trabajo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e8d37-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="e8d37-113">Si es necesario, modifique el archivo de configuración del formulario para reflejar las rutas de acceso actuales de los componentes.</span><span class="sxs-lookup"><span data-stu-id="e8d37-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="e8d37-114">El archivo de configuración del formulario puede contener rutas de acceso relativas, en cuyo caso este paso puede no ser necesario.</span><span class="sxs-lookup"><span data-stu-id="e8d37-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="e8d37-115">Complete los pasos de registro OLE adecuados para asociar el tipo de mensaje con el servidor de formulario que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="e8d37-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="e8d37-116">Si el formulario se instaló en la biblioteca de formularios local, copie el icono del formulario (.ico) y los archivos de configuración (.cfg) en el directorio %WINDOWS%\FORMS\CONFIGS para que el formulario se pueda restaurar automáticamente en caso de que la biblioteca de formularios esté dañada o eliminada.</span><span class="sxs-lookup"><span data-stu-id="e8d37-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="e8d37-117">Este paso se recomienda, pero no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e8d37-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e8d37-118">Puede simplificar la instalación en una biblioteca de formularios local reemplazando los pasos 1 y 2 por una llamada a la [función MAPIOpenLocalFormContainer.](mapiopenlocalformcontainer.md)</span><span class="sxs-lookup"><span data-stu-id="e8d37-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8d37-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8d37-119">See also</span></span>



[<span data-ttu-id="e8d37-120">Desarrollo de servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="e8d37-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

