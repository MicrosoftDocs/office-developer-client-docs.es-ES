---
title: Ejemplo del proveedor de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356591"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="fcdbe-103">Ejemplo del proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="fcdbe-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="fcdbe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcdbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcdbe-105">En este ejemplo se usan archivos y directorios para transmitir y recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="fcdbe-106">Implementa y registra un preprocesador muy simple que anexa una línea de texto a cada mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="fcdbe-107">En el ejemplo se muestra cómo dividir el contenido del mensaje entre el formato de encapsulación neutro de transporte (TNEF) y el texto.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="fcdbe-108">También admite todas las opciones de configuración (hojas de propiedades, asistentes y configuración mediante programación) y opciones de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="fcdbe-109">No admite las interfaces de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="fcdbe-110">Puede descargar este ejemplo de Outlook de código de la API de mensajería [(MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740)</span><span class="sxs-lookup"><span data-stu-id="fcdbe-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fcdbe-111">Ejecutable:</span><span class="sxs-lookup"><span data-stu-id="fcdbe-111">Executable:</span></span>  <br/> |<span data-ttu-id="fcdbe-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="fcdbe-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="fcdbe-113">Directorio de código fuente:</span><span class="sxs-lookup"><span data-stu-id="fcdbe-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="fcdbe-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="fcdbe-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="fcdbe-115">Idioma:</span><span class="sxs-lookup"><span data-stu-id="fcdbe-115">Language:</span></span>  <br/> |<span data-ttu-id="fcdbe-116">C++</span><span class="sxs-lookup"><span data-stu-id="fcdbe-116">C++</span></span>  <br/> |
|<span data-ttu-id="fcdbe-117">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="fcdbe-117">Platforms:</span></span>  <br/> |<span data-ttu-id="fcdbe-118">Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="fcdbe-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="fcdbe-119">Características compatibles</span><span class="sxs-lookup"><span data-stu-id="fcdbe-119">Supported Features</span></span>

<span data-ttu-id="fcdbe-120">En este ejemplo se admiten las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="fcdbe-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="fcdbe-121">Características básicas como el envío, la recepción y el sondeo de nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="fcdbe-122">Configuración interactiva y programática.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="fcdbe-123">La **interfaz IMAPIStatus,** excepto para la configuración de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="fcdbe-124">Para obtener más información, vea la [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="fcdbe-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="fcdbe-125">Seguridad de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-125">Thread safety.</span></span>
    
- <span data-ttu-id="fcdbe-126">Registro de eventos en un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-126">Event logging to a text file.</span></span> <span data-ttu-id="fcdbe-127">El archivo se limita automáticamente a un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="fcdbe-128">Todas las sesiones de transporte usan el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="fcdbe-129">Características no admitidas</span><span class="sxs-lookup"><span data-stu-id="fcdbe-129">Unsupported Features</span></span>

<span data-ttu-id="fcdbe-130">Este ejemplo no admite la detección asincrónica de mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="fcdbe-131">**Para instalar el proveedor de transporte de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="fcdbe-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="fcdbe-132">Para descargar el proveedor de transporte de ejemplo, vea [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="fcdbe-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="fcdbe-133">Busque la carpeta donde guardó los Outlook mapi.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="fcdbe-134">Haga clic con el botón secundario en la **carpeta zip OutlookMAPISamples- \< version \> number** y haga clic en Extraer **todo**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="fcdbe-135">Haga **clic en** Examinar, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **Extraer**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="fcdbe-136">Ejecute Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="fcdbe-137">En Visual Studio 2008, haga **clic** en Archivo , seleccione Abrir **y,** a continuación, haga clic **en Project/Solución**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="fcdbe-138">Vaya a la ubicación donde guardó el ejemplo, haga clic en **mrxp32.vcproj** y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="fcdbe-139">En el menú **Generar,** haga clic **en Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="fcdbe-140">En el cuadro **de diálogo Administrador** de configuración, vaya  a la fila **mrxp32** y, en la columna Configuración, seleccione **Liberar** y, a continuación, haga clic **en Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="fcdbe-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="fcdbe-142">En el **cuadro de diálogo Guardar archivo como,** haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="fcdbe-143">En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en el archivo por lotes de instalación y haga clic **en Ejecutar como administrador.**</span><span class="sxs-lookup"><span data-stu-id="fcdbe-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="fcdbe-144">En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fcdbe-145">**install.bat** copia el .dll a la carpeta de instalación Microsoft Office predeterminada, C:\Archivos de programa\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="fcdbe-146">Si ha instalado productos Office en otra ubicación, haga clic con el botón secundario **eninstall.bat** y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="fcdbe-147">El archivo se abre en Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-147">The file opens in Notepad.</span></span> <span data-ttu-id="fcdbe-148">Reemplace la ruta de instalación predeterminada por la ruta de instalación usada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="fcdbe-149">**Para configurar el proveedor de transporte en Outlook**</span><span class="sxs-lookup"><span data-stu-id="fcdbe-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="fcdbe-150">En el **menú Herramientas** de Outlook, haga clic en **Cuenta Configuración**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="fcdbe-151">En el **cuadro de diálogo Configuración** cuenta, en la pestaña **Correo** electrónico, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="fcdbe-152">En **Elegir servicio de correo electrónico,** haga clic en **Otro**, seleccione Transporte de muestra **de MRXP** y, a continuación, haga clic **en Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="fcdbe-153">En el cuadro de diálogo Configuración de transporte **mrxp** escriba **un nombre para mostrar de usuario**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="fcdbe-154">En **Ruta de acceso a la Bandeja de entrada (recurso compartido UNC)** escriba una ruta de carpeta.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="fcdbe-155">También puede ser una ruta de acceso a una carpeta local.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="fcdbe-156">Esta ruta debe existir.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="fcdbe-157">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="fcdbe-158">En el cuadro **de diálogo Agregar cuenta** de correo electrónico, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="fcdbe-159">Haga clic **en Finalizar** y, a continuación, **en Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="fcdbe-160">Para empezar a usar la cuenta de MRXP, salga y reinicie Outlook.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="fcdbe-161">**Para usar el ejemplo del proveedor de transporte para enviar un mensaje en Outlook**</span><span class="sxs-lookup"><span data-stu-id="fcdbe-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="fcdbe-162">En el **menú Archivo,** haga clic **en Nuevo** y, a continuación, haga clic en Mensaje **de correo**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="fcdbe-163">En el **cuadro Para,** escriba el nombre del destinatario con el formato **[MRXP: \< ADDRESS \> ]**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="fcdbe-164">La dirección es el recurso compartido UNC o la ruta de acceso de carpeta local a la bandeja de entrada del destinatario.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fcdbe-165">Si hay dos puntos o barras diagonales inversas en la dirección, debe insertar una barra diagonal inversa antes de cada dos puntos o barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="fcdbe-166">Por ejemplo, para enviar correo a [MRXP:C:\Mail\myDir] debe escribir  `[MRXP:C\:\\Mail\\myDir]` .</span><span class="sxs-lookup"><span data-stu-id="fcdbe-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="fcdbe-167">La dirección del destinatario debe existir.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="fcdbe-168">Haga **clic en Cuenta** y, a **continuación, en Transporte de ejemplo de MRXP**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="fcdbe-169">Escriba el mensaje y haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-169">Type your message and click **Send**.</span></span> <span data-ttu-id="fcdbe-170">El mensaje se envía mediante el proveedor de transporte MRXP.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="fcdbe-171">**Para usar el ejemplo del proveedor de transporte para recibir un mensaje en Outlook**</span><span class="sxs-lookup"><span data-stu-id="fcdbe-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="fcdbe-172">En el **menú Archivo,** haga clic **en Nuevo** y, a continuación, haga clic en Mensaje **de correo**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="fcdbe-173">Escriba el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-173">Type your message.</span></span>
    
3. <span data-ttu-id="fcdbe-174">Haga clic **en el Microsoft Office,** haga clic en Guardar como y, a continuación, haga clic en Guardar **como** para guardar el archivo en la carpeta de bandeja de entrada que especificó durante la instalación. </span><span class="sxs-lookup"><span data-stu-id="fcdbe-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="fcdbe-175">En el **cuadro de diálogo** Guardar como, busque el recurso compartido UNC o la carpeta local que establezca como bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="fcdbe-176">En la **lista desplegable Guardar como** tipo, haga clic Outlook Formato de **mensaje**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="fcdbe-177">Escriba un nombre para el archivo y haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="fcdbe-178">El archivo se guarda en la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="fcdbe-179">El proveedor de transporte MRXP entrega el mensaje a la Bandeja de entrada en Outlook.</span><span class="sxs-lookup"><span data-stu-id="fcdbe-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

