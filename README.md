# SecurityEngineering-Week6-Ex

TASK 1 :

1. Trusted Platform Module (TPM) 
The Trusted Platform Module (TPM) is a hardware-based security feature designed to secure systems through cryptographic functions. TPMs provide a root of trust by generating, storing, and managing cryptographic keys securely within the hardware. They are commonly used for tasks such as secure boot, disk encryption and ensuring platform integrity.
Security Capabilities:
TPM ensures hardware securely handles cryptographic keys and sensitive operations, protecting against software-based attacks. Ensures that only trusted software can be loaded at boot time, protecting against tampering and malware attacks.TPM securely stores encryption keys and can prevent them from being extracted or tampered with.

Incapabilities:
While TPM provides strong protection against remote attacks, it can be vulnerable to physical tampering, especially in systems where the hardware can be accessed by attackers. TPM alone cannot fully protect software integrity once the operating system has been booted. 

2. Containers
Containers are lightweight, portable units of software that package applications and their dependencies, allowing them to run consistently across various computing environments. Containers share the host system’s kernel, which makes them efficient but poses unique security challenges.
Security Capabilities:
Containers provide process and filesystem isolation using features like namespaces and cgroups. This isolation helps contain attacks within a single container. Compared to virtual machines, containers are more resource-efficient.
Incapabilities:
Since containers share the host’s kernel, a vulnerability in the kernel can affect all containers on the host. Vulnerabilities in container runtimes can lead to container breakout, allowing an attacker to escape and gain access to the host system.

TASK 2 :

To secure the supply chain of a networking hardware and software company, it is critical to address risks across multiple actors involved, such as part suppliers, transportation companies, firmware providers, and internal/external employees. These actors are essential to the manufacture, assembly, and distribution of products like routers. Focusing on each of these key areas can help protect the integrity of the products and minimize the risk of tampering.

For part suppliers, a significant concern is the possibility of receiving tampered components. This can lead to compromised hardware before assembly. To mitigate this risk, implementing Trusted Platform Modules in outsourced components ensures that every part is cryptographically validated. This allows the company to verify that parts have not been altered during manufacturing or transit. Regular supplier audits and certifications to security standards, like ISO/IEC 27001, should be conducted to ensure consistent security practices. Though effective, the challenges include additional costs and the need for smaller suppliers to upgrade their processes.

Firmware providers pose a different set of risks, as compromised software updates can introduce vulnerabilities that expose routers to attacks. Using code-signing ensures that all firmware is authenticated before deployment. Any firmware must be signed with cryptographic keys, adding a layer of protection against unauthorized updates. Additionally, the deployment of Endpoint Detection and Response systems can help detect suspicious activity in firmware once it’s installed. However, the company will need robust cryptographic key management, and the EDR systems may require adjustments to avoid false positives.

Transportation companies handling hardware components and finished products also pose a risk. There is always the possibility of tampering during transit, where malicious actors could intercept and modify hardware. To secure this stage of the supply chain, blockchain-based tracking can be implemented, offering an immutable record of every step of the shipment process. Blockchain makes it difficult to tamper with shipments without leaving a trace. Additionally, using tamper-evident packaging can alert the company if unauthorized access occurs during transit. However, blockchain solutions may not be viable for smaller logistics providers due to their cost and complexity.

Insider threats remain a significant concern, both from in-house and outsourced employees. These employees may have access to sensitive information or may sabotage products intentionally. To address this, User Behavior Analytics can be used to monitor internal activity. By analyzing user behavior, UBA can detect anomalies, such as unauthorized access to systems or data. Limiting access through strict access control policies, where employees only have access to systems they require for their job, can further reduce the risk of insider threats. 

Challenges include working closely with suppliers and transportation companies to implement new security protocols, which may involve offering financial support or training. Security measures like code-signing and blockchain tracking may also introduce operational delays and additional costs, but these investments are crucial for ensuring the safety and integrity of the company’s products.

Managing cryptographic keys for code-signing introduces potential vulnerabilities if those keys are compromised. To minimize this risk, the company must ensure that strong key management practices.
In summary, protecting the supply chain from tampering requires a combination of technology, monitoring, and collaboration with external partners. While there are costs and operational challenges associated with these measures, they are necessary to ensure the security of the products and maintain customer trust. The company must continuously evaluate and adapt its security measures to remain resilient against emerging threats.
