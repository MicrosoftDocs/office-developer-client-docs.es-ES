---
title: Determinar si Outlook es una aplicación de Hacer clic y ejecutar en un equipo
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a710baa4d70ac69b67d2a06fe694998884fd835
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356409"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a><span data-ttu-id="0e9e6-102">Determinar si Outlook es una aplicación de Hacer clic y ejecutar en un equipo</span><span class="sxs-lookup"><span data-stu-id="0e9e6-102">Determine whether Outlook is a Click-to-Run application on a computer</span></span>

<span data-ttu-id="0e9e6-103">Hacer clic y ejecutar es una entrega del software y el mecanismo de actualización disponible para Office 2010 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-103">Click-to-Run is a software delivery and updating mechanism available to Office 2010 and later versions.</span></span> <span data-ttu-id="0e9e6-104">Los productos que se envíen mediante Hacer clic y ejecutar se ejecutan en un entorno virtual de aplicación del sistema operativo local.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-104">Products delivered via Click-to-Run execute in a virtual application environment on the local operating system.</span></span> <span data-ttu-id="0e9e6-105">Esto significa que tienen copias privadas de sus archivos y configuración, y que los cambios que realizan se capturan en el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-105">This means that they have private copies of their files and settings, and that any changes they make are captured in the virtual environment.</span></span>

<span data-ttu-id="0e9e6-106">Hacer clic y ejecutar es rápido, los usuarios pueden iniciar la ejecución de una aplicación en poco tiempo sin tener que esperar que el producto completo finalice la instalación.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-106">Click-to-Run is fast—users can start running an application within a short time without waiting for the complete product to finish installing.</span></span> <span data-ttu-id="0e9e6-107">Las actualizaciones se ejecutan automáticamente en el fondo, sin que un usuario tenga que quitar primero una instalación o instalar actualizaciones de forma manual.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-107">Updates are run automatically in the background, without requiring a user to first remove an installation or manually install updates.</span></span> <span data-ttu-id="0e9e6-108">Los productos de Hacer clic y ejecutar se virtualizan y no entran en conflicto con otro software instalado.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-108">Click-to-Run products are virtualized and do not conflict with other installed software.</span></span> <span data-ttu-id="0e9e6-109">Pero, como un producto entregado por Hacer clic y ejecutar tiene copias privadas de todos sus archivos y del registro, un desarrollador de complementos no puede determinar la existencia del producto de la misma manera que un producto que se instaló en el disco duro del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-109">However, because a product delivered by Click-to-Run has private copies of all its files and registration, an add-in developer cannot determine the product’s existence in the same manner as a product that was installed on a client computer’s hard disk.</span></span> <span data-ttu-id="0e9e6-110">Desde Outlook 2010, los desarrolladores de complementos deben comprobar si Outlook está instalado y si se ha entregado Outlook como un producto de Hacer clic y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-110">Starting with Outlook 2010, add-in developers should verify whether Outlook has been installed, and whether Outlook has been delivered as a Click-to-Run product.</span></span>


> [!NOTE]
> <span data-ttu-id="0e9e6-111">En el entorno de aplicación virtual de Hacer clic y ejecutar solo se admite Office 2013 de 32 bits, incluso si el equipo cliente ejecuta un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0e9e6-111">Only 32-bit Office 2013 is supported in the Click-to-Run virtual application environment, even if the client computer runs a 64-bit operating system.</span></span>



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a><span data-ttu-id="0e9e6-112">Para comprobar si Outlook 2013 se entregó mediante Hacer clic y ejecutar en un equipo cliente</span><span class="sxs-lookup"><span data-stu-id="0e9e6-112">To check whether Outlook 2013 was delivered by Click-to-Run on a client computer</span></span>

- <span data-ttu-id="0e9e6-113">Comprobar si la clave VirtualOutlook existe en la siguiente ubicación del registro de Windows:</span><span class="sxs-lookup"><span data-stu-id="0e9e6-113">Verify whether the VirtualOutlook key exists in the following location in the Windows registry:</span></span>
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  <span data-ttu-id="0e9e6-114">La clave VirtualOutlook es un valor REG\_SZ que contiene la etiqueta de referencia cultural del idioma del producto instalado, como "en-us".</span><span class="sxs-lookup"><span data-stu-id="0e9e6-114">The VirtualOutlook key is a REG\_SZ value that contains the culture tag of the installed product language, such as "en-us".</span></span>

## <a name="see-also"></a><span data-ttu-id="0e9e6-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e9e6-115">See also</span></span>

- [<span data-ttu-id="0e9e6-116">Administración de complementos</span><span class="sxs-lookup"><span data-stu-id="0e9e6-116">Add-in administration</span></span>](add-in-administration.md)

