---
title: Implementación de la interfaz IClassFactory para los servidores de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817706"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="0a7ae-103">Implementación de la interfaz IClassFactory para los servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="0a7ae-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="0a7ae-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a7ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a7ae-105">[IClassFactory](http://msdn.microsoft.com/es-es/library/ms694364%28VS.85%29.aspx) es la interfaz OLE que las aplicaciones cliente que se usan para crear nuevos objetos de formulario de clase de mensaje del servidor de su formulario.</span><span class="sxs-lookup"><span data-stu-id="0a7ae-105">[IClassFactory](http://msdn.microsoft.com/es-es/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="0a7ae-106">En la siguiente tabla se enumera los métodos de **IClassFactory** que son necesarios.</span><span class="sxs-lookup"><span data-stu-id="0a7ae-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="0a7ae-107">**Método**</span><span class="sxs-lookup"><span data-stu-id="0a7ae-107">**Method**</span></span>|<span data-ttu-id="0a7ae-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a7ae-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a7ae-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="0a7ae-109">CreateInstance</span></span>](http://msdn.microsoft.com/es-es/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="0a7ae-110">Crea un nuevo objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="0a7ae-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="0a7ae-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="0a7ae-111">LockServer</span></span>](http://msdn.microsoft.com/es-es/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="0a7ae-112">Bloquea el servidor de formulario en la memoria para que se puede evitar la sobrecarga de inicio cuando se crean varios objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="0a7ae-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="0a7ae-113">Para toda la información necesaria para implementar estos métodos, vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="0a7ae-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0a7ae-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="0a7ae-114">See also</span></span>



[<span data-ttu-id="0a7ae-115">Escritura de código de servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="0a7ae-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

