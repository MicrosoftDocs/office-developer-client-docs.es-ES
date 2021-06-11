---
title: Bibliotecas de formularios personales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420412"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="e8ac1-103">Bibliotecas de formularios personales</span><span class="sxs-lookup"><span data-stu-id="e8ac1-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="e8ac1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8ac1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8ac1-105">Como su nombre indica, las bibliotecas de formularios personales contienen formas de interés para un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="e8ac1-106">La biblioteca de formularios personal de un usuario es la biblioteca de formularios asociada con el almacén de mensajes predeterminado identificado en el perfil del usuario; cada perfil instalado en una estación de trabajo puede usar un almacén predeterminado independiente y, por lo tanto, una biblioteca de formularios personal independiente.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="e8ac1-107">Una biblioteca de formularios personal puede contener copias de formularios que también se encuentran en otras bibliotecas de formularios además de otros formularios.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="e8ac1-108">Una biblioteca de formularios personal se implementa en la tabla de contenido asociado de la carpeta raíz en el almacén de mensajes predeterminado de un usuario, independientemente de si reside en un servidor o localmente en la estación de trabajo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="e8ac1-109">Si el almacén de mensajes predeterminado del usuario se almacena en la estación de trabajo del usuario, las bibliotecas de formularios personales ofrecen un rendimiento mejorado al permitir que las aplicaciones accedan a los formularios localmente en lugar de a través de la red.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="e8ac1-110">También pone los formularios a disposición de los usuarios que trabajan sin conexión, lo que puede ocurrir cuando los usuarios desean llevar sus formularios con ellos en equipos portátiles y no tienen acceso a una red.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="e8ac1-111">Las propiedades y la implementación subyacente de las entradas de biblioteca de formularios personales incluyen una propiedad "Id. de contenedor" que identifica un contenedor maestro con el que se debe sincronizar la entrada local.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="e8ac1-112">Puede ser el identificador de una carpeta arbitraria que contiene formularios.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="e8ac1-113">Esto es útil si usa un administrador de formularios personalizado que admite algún tipo de biblioteca de formularios de toda la organización; el administrador de formularios se encargaría de sincronizar los formularios almacenados en la biblioteca de formularios personal y en la biblioteca de formularios de toda la organización.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="e8ac1-114">Esto probablemente ocurriría cuando se cargó el administrador de formularios, pero teóricamente podría ocurrir en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8ac1-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8ac1-115">See also</span></span>



[<span data-ttu-id="e8ac1-116">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="e8ac1-116">MAPI Forms</span></span>](mapi-forms.md)

