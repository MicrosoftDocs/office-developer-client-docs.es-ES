---
title: Escribir a un cliente automatizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820979"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="71525-103">Escribir a un cliente automatizado</span><span class="sxs-lookup"><span data-stu-id="71525-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="71525-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="71525-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71525-105">Una aplicación cliente automatizada es una aplicación que se ejecute desatendida, no mostrar ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="71525-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="71525-106">De forma predeterminada, muchos de los métodos de interfaz MAPI mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="71525-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="71525-107">Todos estos métodos tienen marcas que permite que un cliente permitir o suprimir esta presentación.</span><span class="sxs-lookup"><span data-stu-id="71525-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="71525-108">Aunque MAPI espera que los proveedores de servicios de cumplimiento de estos marcadores, hay algunos proveedores que no siempre cumplen estas expectativas.</span><span class="sxs-lookup"><span data-stu-id="71525-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="71525-109">Un motivo legítimo para no teniendo en cuenta los indicadores es la dependencia del proveedor de servicios de otro servicio que no permite la supresión de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="71525-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="71525-110">Si está desarrollando a un cliente automatizado, preste especial atención a los proveedores de servicios que se está usando y cómo están configurados.</span><span class="sxs-lookup"><span data-stu-id="71525-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="71525-111">No asuma que todas las llamadas para suprimir una interfaz de usuario se completará correctamente.</span><span class="sxs-lookup"><span data-stu-id="71525-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="71525-112">Clientes automatizados deben tener la información necesaria disponible para la configuración correcta de cada uno de los servicios de mensaje en el perfil.</span><span class="sxs-lookup"><span data-stu-id="71525-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="71525-113">Hay dos formas de proporcionar información de configuración en tiempo de inicio de sesión:</span><span class="sxs-lookup"><span data-stu-id="71525-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="71525-114">El proveedor de servicios puede recuperar información del perfil.</span><span class="sxs-lookup"><span data-stu-id="71525-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="71525-115">El proveedor de servicios puede preguntar al usuario para obtener información.</span><span class="sxs-lookup"><span data-stu-id="71525-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="71525-116">Puesto que la segunda opción es no disponible para los clientes automatizados, estos clientes deben usar la primera opción.</span><span class="sxs-lookup"><span data-stu-id="71525-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="71525-117">Los clientes deben configurar sus perfiles con cuidado para asegurarse de que esta opción siempre funciona.</span><span class="sxs-lookup"><span data-stu-id="71525-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="71525-118">Los clientes automatizados siempre establecer la marca MAPI_NO_MAIL en la llamada a la función [MAPILogonEx](mapilogonex.md) para iniciar una sesión de MAPI.</span><span class="sxs-lookup"><span data-stu-id="71525-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

